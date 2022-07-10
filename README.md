# Splunkbase Release Github Action

This repository provides a github action to publish Splunk Apps and Add-ons to Splunkbase via the [Splunkbase API](https://dev.splunk.com/enterprise/reference/splunkbase/sbreleaseapiref).

## Usage

### Repo structure
The repo must have a `package` folder with your Splunk app contents.

#### Example: repo structure
```
.github/
├─ workflows/
│  ├─ splunkbase_release.yml
package/
├─ default/
├─ metadata/
├─ app.manifest
├─ README
├─ LICENSE
.splunkbase

```

### Example: splunkbase_release.yml
```yaml
name: Release to Splunkbase
on: workflow_dispatch 

jobs:
   publish:
      uses: diogofgm/splunkbase-release-action/.github/workflows/splunkbase-release-action.yml@v0.0.3
      secrets:
         SPLUNKBASE_USER: ${{ secrets.SPLUNKBASE_USER }}
         SPLUNKBASE_PASSWORD: ${{ secrets.SPLUNKBASE_PASSWORD }}

```

### Example: .splunkbase file
```
SPLUNKBASE_ID=XXXX
SPLUNKBASE_SPLUNK_VERSION=8.1,8.2,9.0
SPLUNKBASE_SPLUNK_CIM_VERSION=4.x
```

### Inputs

#### Secrets

* [required] `SPLUNKBASE_USER` - Splunkbase username
* [required] `SPLUNKBASE_PASSWORD` - Splunkbase password
