# ATMOS — Access to medical oxygen scorecard

These tools are implementable versions of the **ATMOS scorecard** as described in the WHO publication [WHO publication URL].

Users may wish to use the implementation on **WHO REDCap** for direct data entry. Please use:
https://extranet.who.int/edcrc/surveys/?s=TML97PKNNTNN8A9Y

> ⚠️ **This repository contains instrument definitions only** — form dictionaries, a REDCap project template and a codebook. It contains **no patient data**, no credentials and no server secrets. Do not commit any of those.

## What's in here

| Path | Contents |
|---|---|
| `CRF/` | The **ODK / KoboToolbox** form dictionary (XLSForm) for the ATMOS scorecard. |
| `REDCap/` | The **REDCap** project (XML) and its **codebook** (PDF) for the ATMOS scorecard. |
| `CHANGELOG.md` | Record of changes to the instruments. |

### Files

- `***` — XLSForm dictionary for ODK/Kobo.
- `***` — importable REDCap project (CDISC ODM).
- `***` — REDCap codebook (field-by-field reference).

## Three ways to collect data

The ATMOS scorecard can be implemented through the following options.

### 1. Direct use of the WHO REDCap implementation

For direct data entry, users may use the WHO REDCap implementation of the scorecard:

https://extranet.who.int/edcrc/surveys/?s=TML97PKNNTNN8A9Y

### 2. ODK / KoboToolbox

**Live reference form:** *** [LINK] ***

To deploy your own copy from the dictionary:

1. Sign in to KoboToolbox (or your ODK Central server).
2. **New → Upload an XLSForm** and select `[FILENAME]`.
3. **Deploy** — Kobo generates the web (Enketo) and mobile (ODK Collect) versions.
4. Validate against the live reference form linked above.

### 3. REDCap

1. In REDCap: **New Project → Upload a REDCap project XML file (CDISC ODM)**.
2. Select `[FILENAME FOR DICTIONARY]`; REDCap builds the instruments and data dictionary.
3. Use `[FILENAME FOR CODEBOOK]` as the reference codebook.
4. Test with dummy data before moving the project to production.

## Get the repository

```bash
git clone https://github.com/WHO-org/who_atmos.git
cd who_atmos
```

*(Replace the organisation/name with the actual repository URL.)*

## Contributing / updating

Work on a branch and open a Pull Request; do not commit directly to `main`. Never commit patient data, credentials, API tokens or record exports.

## Data governance

These instruments are shared to support **medical oxygen ecosystem self-assessment at a national level** and to keep track of progress in the implementation of **WHA resolution 76.3: Increasing access to medical oxygen**. Any data collected with them remains the property of the collecting institution / national programme and is subject to local confidentiality and data-protection rules. Deployment, access control and analysis of collected data are the responsibility of the deploying facility and national programme.

## References

[LINK TO WHO PUBLICATION (DOI)]

https://apps.who.int/gb/ebwha/pdf_files/WHA76/A76_R3-en.pdf

## Maintainer

WHO data team. For access requests or questions, contact the maintainer team (details provided separately, not stored in this repository).
