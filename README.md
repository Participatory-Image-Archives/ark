# PIA Archival Resource Keys (ARKs)
This repository is about how PIA manages its [Archival Resource Keys](https://arks.org/) (ARKs) as persistent identifiers and contains the following parts:

1. ARK Structure
2. ARK Minter
3. ARK Resolver
4. Access persistence policy

## Structure
### General ARK Anatomy

```

  https://example.org/ark:12345/x54xz321/s3/f8.05v.tiff
  \_________________/ \__/ \___/ \______/\____/\_______/
              |        |     |      |      |       |
              |  ARK Label   |      | Sub-parts  Variants
              |              |      |
Name Mapping Authority (NMA) |    Assigned Name
                             |
              Name Assigning Authority Number (NAAN)
```
### The main components of our ARKs

| **ARK main component** | **PIA**                                                     |
|------------------------|-------------------------------------------------------------|
| NMA                    | `https://ark.participatory-archives.ch/`                    |
| NAAN                   | TBD                                                         |
| Assigned Name          | Composed of a shoulder, an identifier and a check character |

## Minter
TBD

## Resolver
TBD

## Access persistence policy
TBD
