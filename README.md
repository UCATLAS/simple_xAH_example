# xAODHelpers - A RootCore Package

## Installing
The last stable analysis base used is **2.1.30**. To install,
```bash
mkdir myRootCore && cd myRootCore
rcSetup Base,2.1.30
git clone https://github.com/UCATLAS/simple_xAH_example
git clone https://github.com/UCATLAS/xAODAnaHelpers
rc checkout_pkg atlasoff/Reconstruction/egamma/egammaMVACalib/tags/egammaMVACalib-01-00-43
rc checkout_pkg atlasoff/Control/xAODRootAccess/tags/xAODRootAccess-00-01-04
source xAODAnaHelpers/scripts/ElectronEfficiencyCorrectionPatch_Base.2.1.30.sh
rc find_packages
rc compile
```

## Running

```xAH_run.py input.root --config=simple_xAH_example/data/simple.json```

## Dependencies
 - dependencies are in [cmt/Makefile.RootCore](cmt/Makefile.RootCore)

### Tested Against AnalysisBase versions:
 - 2.1.30

#### Authors
- [Giordon Stark](https://github.com/kratsg)
