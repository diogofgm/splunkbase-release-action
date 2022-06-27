# Splunkbase Release Github Action

This repository provides a github action to publish Splunk Apps and Add-ons to Splunkbase via the Splunkbase API.

## Usage

```


```

### Inputs

* [required] `.splunkbase` - config file in the repo with the app or add-on details (App ID, supported Splunk and Splunk CIM versions)

```
SPLUNKBASE_ID=4664
SPLUNKBASE_SPLUNK_VERSION=8.1,8.2
SPLUNKBASE_SPLUNK_CIM_VERSION=4.x


### Secrets

* [required] `SPLUNKBASE_USER` - Splunkbase username
* [required] `SPLUNKBASE_PASSWORD` - Splunkbase password
