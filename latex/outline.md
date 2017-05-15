Title: Sensitivity Studies for the Model Unspecific Search
==========================================================

* Introduction (max. 15 pages)
    * Motivation for Particle Physics in General
    * Units and Abbreviations
    * Standard Model
        * Underlying assumptions, Symmetries
        * Lagrangian
        * Particles & Interactions
        * Open Questions, hints for New Physics (refer to other Experiments):
            * Matter/Antimatter Imbalance
            * Dark-Matter Observations (Bullet Cluster)
            * Hierachy Problem
            * Gravity
            * Spin 3/2 Particles
    * BSM
        * Theory of Model1
        * Theory of Model2
    * Experiments (zoom into collider experiments)
    * LHC
    * CMS
        * Detector Geometry and Coordinates
        * Detector Subsystems
        * Triggering
        * Grid (Computing/Storage)


* MUSiC (max 10 pages):
    * Motivation for MUSiC
    * Previous MUSiC Works

    * Definition of Classes (incl., excl., jet incl.)
    * Kinematic Variables + Distributions
        * SumPt
        * InvMass
        * MET

    * MUSiC-Physics Objects, incl. b-jets ?
        * Electron
        * Muon
        * Photons
        * Jets
        * MET

    * RoI-Scanning:
        * Search Space (connected bin regions)
        * Global Significance
        * "extremity" estimator: p-value (normal prior)
        * Treatment of Regions of Low MC Statistics
        * Look-Elsewhere-Effects
            * Regions -> p-tilde
            * Classes -> p-tilde-distrib
            * Distributions -> ?

    * Implementation
        * CMSSW, ROOT, Python/C++
        * Skimming, PXL, TAPAS --> MUSiC
        * MUSiC Workflow (plot)
        * Automation -> Luigi


* Objects and Events (max 5 pages)
    * Event Selection:
        * Used Triggers
        * MET-Filters

    * Object ID + Reco:
        * Offline Reconstruction
        * Identification
        * b/t-Tagging

* Datasets (max 10 pages)
    * SM MC Used (Processes, Reco-Parameters, Triggers)
    * Signal MC Used
    * Signal Mass/Coupling Points

    * Signal Signatures:
        * Gen View (e.g. Resonances)
        * Gen vs. Rec Comparisons

* Systematic Uncertainties (max 5 pages):
    * Considered Uncertainties
    * Treatment of Systematic Uncertainties

---

* Additional studies (max 15 pages)
    * p-value (log-normal prior)
    * Coverage

    * p-hat:
        * Motivation for global p-value
        * Desired Properties and Suggestions

* Sensitivity-Studies (max 40 pages)
    * Results w/o a SM BG
        * Sorted list of RoIs (top 10, larger table in appendix)
        * Selected Event Classes:
            * with largest signal "effect"
            * most significant RoIs
        * Cross-Check: Distribution of p-values per class
        * Distribution of p-tilde-values
        * Distribution of p-hat-values

    * For each Signal Result
        * Results with Current Framework
        * Results with b-jets enabled
        * Results e.g. with better Resolution or different ID
        * Results with higher luminosity (2/fb, 40/fb, 300/fb)

        * Discussion:
            * Discoverability (why)

    * Discussion of Results:
        * Possible further improvements on CMS/MUSiC


* Conclusion (max 5 pages):
    * What did I do:
        * Implement and Establish Validation Framework

    * State of CMS data taking, plans until 20XX (->improvements planned?)
    * State of MUSiC Analysis

* Literature

* Appendix


BSM Models
==========

* E-Mu QBH (Lepton Flavor Violating t-channel): EXO-16-001 (P) / AN-2015/191, EXO-16-058 / AN-2016/163
    - Sample: QBHToEMu, RPVresonantToEMu ... LLE
    - RPV->e mu
        + x-secs in der DB und AN sind falsch (in AN stehen pb, gemeint sind fb = angegebene xsecs Faktor 1000 zu groß)
        + Public (2015) Exp Limit LQD001: 1000 GeV, LQD01 2700GeV, LQD02 3300GeV
        + Private Exp Limits LQD001: 1.76 TeV, LQD01 3.72TeV
        + Mass/Coupling points:
            * LQD 0.01: 200 GeV, 1000 GeV, 1400 GeV

    - QBHToEMu:
        + Exp Limit dim4-6: 4300 GeV
        + Mass/Dim points:
            * n4: 3000 GeV, 4000 GeV, 5000 GeV

* Semi-Classical-BH (non-resonant, but high multiplicities): EXO-15-007 (P) / AN-2015/130
    - Private Samples (see https://twiki.cern.ch/twiki/bin/view/CMS/BHAnalysis2015Samples )
    - Black hole types:
        + BH1: No tension, non-rotating << THIS I WANT
        + BH2: Rotating, non-split dimensions, no gravitons in FinalBurst (?)
        + BH5: like BH2, but with gravitons in FinalBurst
    - I should take BH1, n=6, MD=4TeV, as this is one benchmark model in EXO-15-007
        + Expected Limit BH1_n6_MD4000: MBH=8.7 TeV
        + Cross Sections: https://twiki.cern.ch/twiki/bin/view/CMS/BlackHoleAnalysis2015#Signal_samples -> https://docs.google.com/spreadsheets/d/1UYe-w-IUYycUqRsyA7INpV_vI5F0Q1KiT50iqX9DIFM/edit#gid=1691832654

* Seesaw (lll etc): EXO-16-002 (P) / AN-2015/256, EXO-17-006 (P) / AN-2016/192
    - SeesawTypeIII_*
    - Exp Limit at 790 GeV
    - Mass points 380, 500 GeV
    - Cross Sections: ???

* W' to TB: B2G-17-010 (P) / AN-2016/480
    - Limits: MW' >> Mnu: 3.3 TeV, MW' < Mnu: 3.5 TeV (expected)
    - Mass points: 2, 3, 3.5, 4 TeV
    - Cross Sections in AN, but not in Lep/Had

===
Sample List:

RPVresonantToEMu_M-200_LLE_LQD-001:
    RPVresonantToEMu_M-200_LLE_LQD-001_13TeV_CA

RPVresonantToEMu_M-1000_LLE_LQD-001:
    RPVresonantToEMu_M-1000_LLE_LQD-001_13TeV_CA

RPVresonantToEMu_M-1400_LLE_LQD-001:
    RPVresonantToEMu_M-1400_LLE_LQD-001_13TeV_CA

RPVresonantToEMu_M-4000_LLE_LQD-02:
    RPVresonantToEMu_M-4000_LLE_LQD-02_13TeV_CA

RPVresonantToEMu_M-5000_LLE_LQD-02:
    RPVresonantToEMu_M-5000_LLE_LQD-02_13TeV_CA

RPVresonantToEMu_M-6500_LLE_LQD-02:
    RPVresonantToEMu_M-6500_LLE_LQD-02_13TeV_CA

QBHToEMu_M-3000_n4:
    QBHToEMu_M-3000_n4_ADD-QBH_13TeV_P8

QBHToEMu_M-4000_n4:
    QBHToEMu_M-4000_n4_ADD-QBH_13TeV_P8

QBHToEMu_M-5000_n4:
    QBHToEMu_M-5000_n4_ADD-QBH_13TeV_P8

SeesawTypeIII_M-380:
    SeesawTypeIII_SIGMAplusSIGMA0HH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZW_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0HZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WH_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0HW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0HW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZW_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HW_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZH_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0HZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WH_M-380_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZZ_M-380_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0HH_M-380_13TeV_MG

SeesawTypeIII_M-500:
    SeesawTypeIII_SIGMA-SIGMA0HH_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZH_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0HZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WW_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WH_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0HH_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WH_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0HW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0HW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WH_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZH_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZH_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0ZZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0ZZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-ZZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-WW_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA-HH_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0WW_M-500_13TeV_MG
    SeesawTypeIII_SIGMA-SIGMA0HZ_M-500_13TeV_MG
    SeesawTypeIII_SIGMAplusSIGMA0WZ_M-500_13TeV_MG



Lumi 2015 ( https://cds.cern.ch/record/2138682?ln=de ):
    2.3 fb

Lumi 2016:
    35.9 /fb

#Lumi predicted for 2017 ( https://lhc-commissioning.web.cern.ch/lhc-commissioning/performance/2017-performance.htm ):
#    45-60 /fb

Lumi Run II:
    100 /fb

#HL-LHC ( http://hilumilhc.web.cern.ch/about/lhc-baseline#overlay-context=about/hl-lhc-project ):
#    up to 3000 /fb




FINAL SIGNALS:
    * Semi-Classical BH
    * RPV->e+mu
    * QBH->e+mu
    * Seesaw


Seesaw 380 ablesen:
* Plot: 0.22pb
* DB: 0.06188
* Faktor: 3.56

Seesaw 500 ablesen:
* Limit Plot: M=500, xsec: 6.4e-2 pb
* CSV: 0.01891=1.891e-2 pb
* => Faktor 3.38