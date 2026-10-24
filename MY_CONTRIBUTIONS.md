# My Contributions to RustGIS

This repository is my personal copy of [RustGIS](https://github.com/opengeos/RustGIS). This file records my contributions to the project.

## Bengali interface localization

- Added Bengali (`bn`) as a selectable interface language, displayed as **বাংলা**.
- Added the Bengali translation catalog at `crates/ui-egui/src/i18n/bn.tsv`.
- Registered Bengali as its own script in the localization and font-discovery paths.
- Added glyph-coverage handling for Bengali fonts discovered on desktop systems.
- Kept the web font URL unset for Bengali because no verified, appropriately licensed web font source was established.

The contribution was submitted in [opengeos/RustGIS pull request #803](https://github.com/opengeos/RustGIS/pull/803) and merged into the upstream project.

### Rendering note

The current font path can discover Bengali-capable fonts and check glyph coverage, but this does not establish correct Indic conjunct shaping. Bengali rendering should be considered subject to the shaping support of the current rendering stack; this contribution did not add a new shaping engine or bundle a font.
