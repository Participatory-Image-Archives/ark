# PIA Archival Resource Keys (ARKs)
This repository is about how PIA manages its [Archival Resource Keys](https://arks.org/) (ARKs) as persistent identifiers and contains the following parts:

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
### Main ARKs

| **NMA and Base Compact Name** | **PIA**                                                     |
|------------------------|-------------------------------------------------------------|
| Name Mapping Authority (NMA)                    | `https://ark.participatory-archives.ch/`                    |
| Label                  | `ark:`                                                         |
| Name Assigning Authority Number (NAAN)                   | TBD                                                         |
| Shoulder         | One for each sub-domain |
| Blade         | Object Identifier appended by a check character |

#### PIA ARK Shoulders
TBD

#### Examples
TBD

## Minter
TBD

## Resolver
TBD

## Access persistence policy
TBD
