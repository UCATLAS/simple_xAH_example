# A Simple xAH Example

## Installing
The last stable analysis base used is **2.3.14**. To install,
```bash
export ATLAS_LOCAL_ROOT_BASE=/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase
alias setupATLAS='source ${ATLAS_LOCAL_ROOT_BASE}/user/atlasLocalSetup.sh'
source ${ATLAS_LOCAL_ROOT_BASE}/user/atlasLocalSetup.sh
mkdir myRootCore && cd myRootCore
rcSetup Base,2.3.14
git clone https://github.com/UCATLAS/simple_xAH_example
git clone https://github.com/UCATLAS/xAODAnaHelpers
python xAODAnaHelpers/scripts/checkoutASGtags.py 2.3.14
rc find_packages
rc compile
```

## Running

```xAH_run.py input.root --config=simple_xAH_example/data/simple.json```

This will produce two sets of plots, one for the input `AntiKt4LCTopoJets` that you are applying JetSelector on, and one for the output `AntiKt4LCTopoJets` that have passed the pre-selection.

For other options, run `xAH_run.py -h` but note that only direct driver has been tested right now.

## Dependencies
 - dependencies are in [cmt/Makefile.RootCore](cmt/Makefile.RootCore)

### Tested Against AnalysisBase versions:
 - 2.3.14

#### Authors
- [Giordon Stark](https://github.com/kratsg)
