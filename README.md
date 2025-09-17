This code is used for an efficiency analysis for B->Dh decays in CMS.
The decays studied are B->DK and B-Dpi, with the D mesons that decays in KK, pipi or Kpi.

The code (use fast_code.ipynb since it's the fastest and the most updated) is implemented in such a way that you can analyze one of the six combinations by choosing the right parameters in the beginning.
You need to choose the right path to put in the folder variable between:

/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_Dpi_Kpipi_Run3Summer24NanoAOD_v0_2025Aug27/B_to_Dpi_Kpipi__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_Dpi_Kpipi__Run3Summer24NanoAOD_v0/250827_105135
/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_DK_KpiK_Run3Summer24NanoAOD_v0_2025Aug27/B_to_DK_KpiK__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_DK_KpiK__Run3Summer24NanoAOD_v0/250827_105043
/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_Dpi_pipipi_Run3Summer24NanoAOD_v0_2025Aug27/B_to_Dpi_pipipi__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_Dpi_pipipi__Run3Summer24NanoAOD_v0/250827_105152
/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_DK_KKK_Run3Summer24NanoAOD_v0_2025Aug27/B_to_DK_KKK__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_DK_KKK__Run3Summer24NanoAOD_v0/250827_105026
/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_Dpi_KKpi_Run3Summer24NanoAOD_v0_2025Aug27/B_to_Dpi_KKpi__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_Dpi_KKpi__Run3Summer24NanoAOD_v0/250827_105118
/eos/user/f/fsimone/B_Dh_summerproject/bphnano/B_to_DK_pipiK_Run3Summer24NanoAOD_v0_2025Aug27/B_to_DK_pipiK__TuneCP5_13p6TeV_pythia8_Run3Summer24GS_v1/B_to_DK_pipiK__Run3Summer24NanoAOD_v0/250827_105101

You need to write the sequence of final states for your decay in the same order of the path name and put it in the "decay" variable.
Then you need to change id3 to the absolute value of the pdg Id of the B-daughter final state, and you need to put in id1 and id2 the pdg Id of the two D daughters.
For decays where D decays in two equal particles, you need to put only one value in id1 and one value in id2, with the correct sign.
For decays where D decays in K pi, you need yo put the positive and negative value of the pdgId of the daughter in both id1 and id2.
Set t to True if you want to cut the events without a muon with pt>9 and abs(eta)<2.4

