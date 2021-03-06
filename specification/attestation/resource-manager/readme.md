# Attestation
    
> see https://aka.ms/autorest

This is the AutoRest configuration file for Attestation.



---
## Getting Started 
To build the SDK for Attestation, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information 
These are the global settings for the Attestation API.

``` yaml
openapi-type: arm
tag: package-2018-09-preview
```

### Tag: package-2018-09-preview

These settings apply only when `--tag=package-2018-09-preview` is specified on the command line.

``` yaml $(tag) == 'package-2018-09-preview'
input-file:
- Microsoft.Attestation/preview/2018-09-01-preview/attestation.json
```

---
# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-net
  - repo: azure-sdk-for-python
```

## Python

See configuration in [readme.python.md](./readme.python.md)

---
## C# 

These settings apply only when `--csharp` is specified on the command line.
Please also specify `--csharp-sdks-folder=<path to "SDKs" directory of your azure-sdk-for-net clone>`.

``` yaml $(csharp)
csharp:
  azure-arm: true
  license-header: MICROSOFT_MIT_NO_VERSION
  namespace: Microsoft.Azure.Management.Attestation
  output-folder: $(csharp-sdks-folder)/attestation/Microsoft.Azure.Management.Attestation/src/Generated
  clear-output-folder: true
```



## Multi-API/Profile support for AutoRest v3 generators 

AutoRest V3 generators require the use of `--tag=all-api-versions` to select api files.

This block is updated by an automatic script. Edits may be lost!

``` yaml $(tag) == 'all-api-versions' /* autogenerated */
# include the azure profile definitions from the standard location
require: $(this-folder)/../../../profiles/readme.md

# all the input files across all versions
input-file:
  - $(this-folder)/Microsoft.Attestation/preview/2018-09-01-preview/attestation.json

```

If there are files that should not be in the `all-api-versions` set, 
uncomment the  `exclude-file` section below and add the file paths.

``` yaml $(tag) == 'all-api-versions'
#exclude-file: 
#  - $(this-folder)/Microsoft.Example/stable/2010-01-01/somefile.json
```

