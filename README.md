# Splunkbase Release Github Action

This repository provides a github action to publish Splunk Apps and Add-ons to Splunkbase via the [Splunkbase API](https://dev.splunk.com/enterprise/reference/splunkbase/sbreleaseapiref).

## Usage

```


```

### Inputs

* [required] `.splunkbase` - config file in the repo with the app or add-on details (App ID, supported Splunk and Splunk CIM versions)

#### Example .splunkbase file
```
SPLUNKBASE_ID=XXXX
SPLUNKBASE_SPLUNK_VERSION=8.1,8.2,9.0
SPLUNKBASE_SPLUNK_CIM_VERSION=4.x
```

### Secrets

* [required] `SPLUNKBASE_USER` - Splunkbase username
* [required] `SPLUNKBASE_PASSWORD` - Splunkbase password
