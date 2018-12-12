# flist-builder-config
debug autobuilder config template



## How to use it

### Create project
Create a directory (organization_name/project_name)

### Add branches you want to build against
Branches bunch of YAML files `BRANCH_NAME.yaml` (e.g to add autobuilder on master branch of your project you create `MY_ORG/MY_PROJ/master.yaml` file)

### Branch build instructions
In the YAML file (e.g master.yaml) you define the `buildscripts` (entry point script exists in your github project)

```yaml
buildscripts:
 - autobuild/tfchain.sh

autobuild/tfchain.sh:
  archives: /tmp/archives
  artifact: tfchain.tar.gz
```

and for each buildscript you define
- artifact: uploaded tar.gz file name
- archives: where the artifact will be created

## Watching the build process

Build monitoring exists here https://build.grid.tf


## Getting the flists

Flists will be generated here https://hub.grid.tf/tf-autobuilder