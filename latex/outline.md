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

* MUSiC (max 10 pages):
    * Motivation for MUSiC
    * Previous MUSiC Theses

    * MUSiC-Physics Objects, incl. b-jets ?
    * Definition of Classes (incl., excl., jet incl.)
    * Kinematic Variables + Distributions

    * RoI-Scanning:
        * Motivation (many classes, automated search necessary)
        * Search Space (connected bin regions)
        * p-value (normal prior)
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

* E-Mu QBH (Lepton Flavor Violating t-channel): EXO-16-001
* Semi-Classical-BH (non-resonant, but high multiplicities): EXO-15-007
* Seesaw (lll etc): EXO-16-002
* RPV-SUSY (resonant)

