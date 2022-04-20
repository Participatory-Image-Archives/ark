# PIA Archival Resource Keys (ARKs)
This repository is about how PIA manages its Archival Resource Keys (ARKs) as persistent identifiers and contains the following parts:

1. ARK Structure
2. ARK Minter
3. ARK Resolver
4. Access persistence policy

## Structure
### General ARK Anatomy

```
                        Base Compact Name   Qualifiers
                           _________________  ___________
                          /                 \/           \
      https://example.org/ark:12345/x6np1wh8k/c3/s5.v7.xsl
              \_________/ \__/\___/\_/\_____/\____/\_____/
                 NMA     Label NAAN |  Blade Parts Variants
                                  Shoulder
                              \_____________/
                                 Check Zone

```
### Main components of PIA ARKs

| **NMA and Base Compact Name** | **PIA**                                                     |
|------------------------|-------------------------------------------------------------|
| Name Mapping Authority (NMA)                    | `https://ark.participatory-archives.ch/`                    |
| Label                  | `ark:`                                                         |
| Name Assigning Authority Number (NAAN)                   | `19156`                                                         |
| Shoulder         | A three-character prefix depending on sub-domains and object types such as `bnz` (cf. below) |
| Blade         | Object Identifier appended by a check character |

#### PIA ARK Shoulders

| **Shoulder** |  Use            | **PIA (sub)-domain**                                         |
|--------------|-----------------|--------------------------------------------------------------|
|  bnz         | Object              | `https://participatory-archives.ch/`                         |
|  czn         | Person              | `https://participatory-archives.ch/`                         |
|  dtf         | PIA API Object      | `https://data.participatory-archives.ch/`                    |
|  dtg         | PIA API Person      | `https://data.participatory-archives.ch/`                    |
|  tkt         | Vocabulary Term     | `https://vocab.participatory-archives.ch/`                   |
|  rpz         | IIIF Resource       | `https://iiif.participatory-archives.ch/`                    |

#### Examples

|                   | **ARK**               | **Landing Page**                                             |
|-------------------|-----------------------|--------------------------------------------------------------|
| **PIA**           | `ark:19156/bnz14759x` | `https://participatory-archives.ch/object/14759` (still _images_ for the moment)             |
| **PIA API**       | `ark:19156/dtf14759y` | `https://data.participatory-archives.ch/object/14759`        |
| **IIIF Manifest** | `ark:19156/rpz14759z` | `https://iiif.participatory-archives.ch/14759/manifest.json` |

## Minter
TBD

## Resolver
TBD

`https://ark.participatory-archives.ch/ark:19156/bnz14759x` as well as `https://n2t.net/ark:19156/bnz14759x` should redirect to `https://participatory-archives.ch/images/14759`

## Access persistence policy
TBD

## References
- [The ARK Identifier Scheme](https://datatracker.ietf.org/doc/html/draft-kunze-ark-34)
- [Archival Resource Key Alliance](https://arks.org/)
- [Name Assigning Authority Number (NAAN) Registry](https://n2t.net/e/pub/naan_registry.txt)
- [Nice Opaque IDentifier (NOID)](http://n2t.net/e/noid.html)
