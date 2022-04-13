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
| Name Assigning Authority Number (NAAN)                   | TBD                                                         |
| Shoulder         | One for each sub-domain |
| Blade         | Object Identifier appended by a check character |

#### PIA ARK Shoulders

| **Shoulder** | **PIA (sub)-domain**                       |
|---------------|--------------------------------------------|
| TBD           | `https://participatory-archives.ch/`       |
| TBD           | `https://data.participatory-archives.ch/`  |
| TBD           | `https://vocab.participatory-archives.ch/` |

#### Examples
TBD

## Minter
TBD

## Resolver
TBD

## Access persistence policy
TBD

## References
- [The ARK Identifier Scheme](https://datatracker.ietf.org/doc/html/draft-kunze-ark-34)
- [Archival Resource Key Alliance](https://arks.org/)
- [Name Assigning Authority Number (NAAN) Registry](https://n2t.net/e/pub/naan_registry.txt)
- [Nice Opaque IDentifier (NOID)](http://n2t.net/e/noid.html)
