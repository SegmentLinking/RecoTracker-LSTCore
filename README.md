# RecoTracker-LSTCore

This repository contains the geometry and module map inputs required by the `RecoTracker/LSTCore` package. These files are generated with the `DumpLSTGeometry` analyzer of the CMSSW `RecoTracker/LSTGeometry` package, so that they are the same as the maps that CMSSW builds from the tracker geometry at run time (earlier versions were generated from the [LSTGeometry](https://github.com/SegmentLinking/LSTGeometry) repository). They are organized by their outer tracker (OT) and inner tracker (IT) version. The suffix `ptXX` indicates the pT cut (in GeV) used to generate the module map and pixel map.

To regenerate them, in a CMSSW area:

    cmsRun RecoTracker/LSTGeometry/test/dumpLSTGeometry.py --geometry Run4D121 --ptCut 0.8 --binaryOutput --outputDirectory OT800_IT615_pt0.8
    cmsRun RecoTracker/LSTGeometry/test/dumpLSTGeometry.py --geometry Run4D121 --ptCut 0.6 --binaryOutput --outputDirectory OT800_IT615_pt0.6

## Current Geometry Versions

- OT800_IT615 : [Tracker Version OT800_IT615](https://cms-tklayout.web.cern.ch/cms-tklayout/layouts-work/recent-layouts/OT800_IT615/info.html) ([same as T24](https://github.com/cms-sw/cmssw/blob/master/Configuration/Geometry/README.md#phase-2-geometries))
