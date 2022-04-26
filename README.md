# Foreword
For the PIA research project, we would like to have, as much as possible, consistent URI schemas. For this purpose, we set up quite a few sub-domains (as shown in the table below).

| **Type**                                                           | **URI example**                                 |
|----------------------------------------------------------------|----------------------------------------------------|
| Digital representation of an object (with content negotiation) | `https://participatory-archives.ch/entity/<ID>`           |
| PIA central API                                                | `https://data.participatory-archives.ch/api/v1/entity/<ID>`      |
| Linked Art API                                                 | `https://linkedart.participatory-archives.ch/entity/<ID>` |
| IIIF Image API                                                 | `https://sipi.participatory-archives.ch/<ID>/info.json`                   |
| IIIF Presentation API (Manifest/Collection)                               | `https://iiif.participatory-archives.ch/<ID>/manifest.json`                |
| Controlled Vocabularies                                            | `https://vocab.participatory-archives.ch/vocabulary/<ID>`      |
| Project Website                                            | `https://project.participatory-archives.ch/`      |

To avoid link rot, we are going to leverage Archival Resource Keys (ARKs) as persistent identifiers.

# PIA Archival Resource Keys (ARKs)
For the management of the PIA ARKs, the following parts are described in this repository:

- ARK Structure
- ARK Minter
- ARK Resolver
- Access persistence policy

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

| **NMA and Base Compact Name**            | **PIA**                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------|
| Name Mapping Authority (NMA)             | `https://ark.participatory-archives.ch/`                                                     |
| Label                                    | `ark:`                                                                                       |
| Name Assigning Authority Number (NAAN)   | `19156`                                                                                      |
| Shoulder                                 | A three-character prefix depending on sub-domains and entity types such as `bnz` (cf. below) |
| Blade                                    | Object Identifier appended by a check character                                              |

#### PIA ARK Shoulders

| **Shoulder** |  Use                             | **PIA (sub)-domain and entity**                              |
|--------------|----------------------------------|--------------------------------------------------------------|
|  bnz         | Object                           | `https://participatory-archives.ch/object/`                  |
|  czn         | Agent                            | `https://participatory-archives.ch/agent/`                   |
|  dtf         | PIA API Object                   | `https://data.participatory-archives.ch/api/v1/object/`      |
|  dtg         | PIA API Agent                    | `https://data.participatory-archives.ch/api/v1/agent/`       |
|  ztf         | Linked Art API Object            | `https://linkedart.participatory-archives.ch/object/`        |
|  ztg         | Linked Art API Agent             | `https://linkedart.participatory-archives.ch/agent/`         |
|  tkt         | Vocabulary Term                  | `https://vocab.participatory-archives.ch/`                   |
|  cpz         | IIIF Image API                   | `https://sipi.participatory-archives.ch/`                    |
|  rpz         | IIIF Presentation API Resource   | `https://iiif.participatory-archives.ch/`                    |

#### Examples

|                   | **ARK**               | **Landing Page**                                             |
|-------------------|-----------------------|--------------------------------------------------------------|
| **PIA**           | `ark:19156/bnz14759z` | `https://participatory-archives.ch/object/14759`             |
| **PIA API**       | `ark:19156/dtf14759z` | `https://data.participatory-archives.ch/api/v1/object/14759` |
| **Linked Art API**| `ark:19156/ztf14759z` | `https://linkedart.participatory-archives.ch/object/14759`   |
| **IIIF Manifest** | `ark:19156/rpz14759z` | `https://iiif.participatory-archives.ch/14759/manifest.json` |

## Minter
TBD

## Resolver
TBD

`https://ark.participatory-archives.ch/ark:19156/bnz14759z` as well as `https://n2t.net/ark:19156/bnz14759z` should redirect to `https://participatory-archives.ch/images/14759`

## Access persistence policy
TBD

## References
- [The ARK Identifier Scheme](https://datatracker.ietf.org/doc/html/draft-kunze-ark-34)
- [Archival Resource Key Alliance](https://arks.org/)
- [Name Assigning Authority Number (NAAN) Registry](https://n2t.net/e/pub/naan_registry.txt)
- [Nice Opaque IDentifier (NOID)](http://n2t.net/e/noid.html)
