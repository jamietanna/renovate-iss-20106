# Renovate reproduction case - Dockerfile manager doesn't understand rc versioning

Reproduction for https://github.com/renovatebot/renovate/issues/20106

# Actual

```
DEBUG: packageFiles with updates (repository=jamietanna/renovate-iss-20106, baseBranch=main)
       "config": {
         "dockerfile": [
           {
             "packageFile": "Dockerfile",
             "deps": [
               {
                 "depName": "whitesource/renovate",
                 "currentValue": "3.0.0-rc.0",
                 "replaceString": "whitesource/renovate:3.0.0-rc.0",
                 "autoReplaceStringTemplate": "{{depName}}{{#if newValue}}:{{newValue}}{{/if}}{{#if newDigest}}@{{newDigest}}{{/if}}",
                 "datasource": "docker",
                 "depType": "final",
                 "depIndex": 0,
                 "updates": [],
                 "warnings": [],
                 "versioning": "docker",
                 "sourceUrl": "https://github.com/whitesource/renovate-on-prem",
                 "registryUrl": "https://index.docker.io",
                 "changelogUrl": "https://github.com/whitesource/renovate-on-prem",
                 "currentVersion": "3.0.0",
                 "fixedVersion": "3.0.0-rc.0"
               }
             ]
           }
         ]
       }
```

And no PR raised.

# Expected

An upgrade to `3.0.0` is expected
