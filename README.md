# Dengue Light CRF — clinical data-capture instruments

Companion repository to the WHO report *Streamlined dengue clinical data capture in the hospital setting – case report form*.

This repository distributes the **instruments** for a harmonised, lightweight dengue clinical case report form (CRF): a minimal-burden data-collection tool for **routine** hospital care (not research-grade complexity), designed to generate near real-time insight into dengue severity, care processes, outcomes and service pressures. Data elements are mapped to existing standards (ICD-11, OMOP) so collected data can feed secure, interoperable infrastructure aligned with existing research tools.

> ⚠️ **This repository contains instrument definitions only** — form dictionaries, a REDCap project template and a codebook. It contains **no patient data**, no credentials and no server secrets. Do not commit any of those.

## What's in here

| Path | Contents |
|---|---|
| `CRF/` | The **ODK / KoboToolbox** form dictionary (XLSForm) for the Light Dengue CRF. |
| `REDCap/` | The **REDCap** project (XML) and its **codebook** (PDF) for data collection. |
| `docs/` | Supporting notes and figures (optional). |
| `SOP_repository_setup_and_maintenance.md` | How this repository is created, maintained and updated. |
| `CHANGELOG.md` | Record of changes to the instruments. |

### Files

- `CRF/DENGUE_ODK_updated.v7.8.4 1.xlsx` — XLSForm dictionary for ODK/Kobo.
- `REDCap/DengueLightCRF_2026-07-30_1357.REDCap.xml` — importable REDCap project (CDISC ODM).
- `REDCap/Dengue - LightCRF _ REDCap.pdf` — REDCap codebook (field-by-field reference).

## Two ways to collect data

The same CRF is provided for two widely used platforms so facilities can use whichever they already run.

### 1. ODK / KoboToolbox

**Live reference form:** https://ee.kobotoolbox.org/x/3WN8CVM5

To deploy your own copy from the dictionary:

1. Sign in to KoboToolbox (or your ODK Central server).
2. **New → Upload an XLSForm** and select `CRF/DENGUE_ODK_updated.v7.8.4 1.xlsx`.
3. **Deploy** — Kobo generates the web (Enketo) and mobile (ODK Collect) versions.
4. Validate against the live reference form linked above.

Optional local check before upload:

```bash
pip install pyxform
xls2xform "CRF/DENGUE_ODK_updated.v7.8.4 1.xlsx" /tmp/dengue_form.xml
```

### 2. REDCap

1. In REDCap: **New Project → Upload a REDCap project XML file (CDISC ODM)**.
2. Select `REDCap/DengueLightCRF_2026-07-30_1357.REDCap.xml`; REDCap builds the instruments and data dictionary.
3. Use `REDCap/Dengue - LightCRF _ REDCap.pdf` as the reference codebook.
4. Test with dummy data before moving the project to production.

## Get the repository

```bash
git clone https://github.com/WHO-org/dengue-light-crf.git
cd dengue-light-crf
```

*(Replace the organisation/name with the actual repository URL. Access is restricted; you must be added to the WHO team.)*

## Contributing / updating

Work on a branch and open a Pull Request; do not commit directly to `main`. Never commit patient data, credentials, API tokens or record exports.

## Data governance

These instruments are shared to support routine dengue clinical data capture and quality improvement. Any data collected with them remains the property of the collecting institution / national programme and is subject to local confidentiality and data-protection rules. Deployment, access control and analysis of collected data are the responsibility of the deploying facility and national programme.

## Standards & interoperability

CRF data elements are mapped to **ICD-11** and **OMOP**, supporting interoperability with existing surveillance and research infrastructure and enabling comparable, harmonised reporting across facilities and countries.

## References

WHO dengue dashboard; WHO dengue clinical management guidelines; ISARIC clinical characterisation tools and core outcome sets. See the main report for the full reference list.

## Maintainer

WHO data team. For access requests or questions, contact the maintainer team (details provided separately, not stored in this repository).
