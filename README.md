# A Simple xAH Example

## Installing
The last stable analysis base used is **2.3.12**. To install,
```bash
export ATLAS_LOCAL_ROOT_BASE=/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase
alias setupATLAS='source ${ATLAS_LOCAL_ROOT_BASE}/user/atlasLocalSetup.sh'
source ${ATLAS_LOCAL_ROOT_BASE}/user/atlasLocalSetup.sh
mkdir myRootCore && cd myRootCore
rcSetup Base,2.3.12
git clone https://github.com/UCATLAS/simple_xAH_example
git clone https://github.com/UCATLAS/xAODAnaHelpers
cd xAODAnaHelpers && git checkout simple_xAH_example_branch && cd ../
rc find_packages
rc compile
```

## Running

```xAH_run.py input.root --config=simple_xAH_example/data/simple.json```

For other options, run `xAH_run.py -h` but note that only direct driver has been tested right now.

## Dependencies
 - dependencies are in [cmt/Makefile.RootCore](cmt/Makefile.RootCore)

### Tested Against AnalysisBase versions:
 - 2.3.12

#### Authors
- [Giordon Stark](https://github.com/kratsg)
