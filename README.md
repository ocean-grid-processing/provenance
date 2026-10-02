# provenance
provenance records for OHC pipeline runs.

## 260921-OP20260507

First runs including support for intensive variables like mixed layer depth, and support for the generic field emitter.

- Input: LocalGP [run OP20260507](https://github.com/argovis/ocean_pipeline/tree/main/provenance/localGP#op20260507-series)
- Pipeline code:
  - localgp_ogp_ingest: https://github.com/ocean-grid-processing/localgp_ogp_ingest/releases/tag/1.1.0
  - ogp_derive: https://github.com/ocean-grid-processing/ogp_derive/releases/tag/1.1.0
  - ohca_ohu_ogp_emitter: https://github.com/ocean-grid-processing/ohca_ohu_ogp_emitter/releases/tag/1.0.0
  - gcos_ogp_emitter: https://github.com/ocean-grid-processing/gcos_ogp_emitter/releases/tag/1.1.0
  - map_ogp_emitter: https://github.com/ocean-grid-processing/map_ogp_emitter/releases/tag/1.0.0
  - field_map_ogp_emitter: https://github.com/ocean-grid-processing/field_map_ogp_emitter/releases/tag/1.0.0 and 1.1.0; see file metadata.
- Pipeline environment: https://github.com/ocean-grid-processing/provenance/blob/main/environments/ohc_crosscheck

## 260908-OP20260507

First production run; data released as https://doi.org/10.5281/zenodo.22757913.

- Input: LocalGP [run OP20260507](https://github.com/argovis/ocean_pipeline/tree/main/provenance/localGP#op20260507-series)
- Pipeline code:
  - localgp_ogp_ingest: https://github.com/ocean-grid-processing/localgp_ogp_ingest/releases/tag/1.0.0
  - ogp_derive: https://github.com/ocean-grid-processing/ogp_derive/releases/tag/1.0.0
  - ohca_ohu_ogp_emitter: https://github.com/ocean-grid-processing/ohca_ohu_ogp_emitter/releases/tag/1.0.0
  - gcos_ogp_emitter: https://github.com/ocean-grid-processing/gcos_ogp_emitter/releases/tag/1.0.0
  - map_ogp_emitter: https://github.com/ocean-grid-processing/map_ogp_emitter/releases/tag/1.0.0
- Pipeline environment: https://github.com/ocean-grid-processing/provenance/blob/main/environments/ohc_crosscheck
- Runbook notes: each pipeline step has a `run.sh` to manage slurm scheduling on CU Blanca; set parameters therein, as well as in the top-level `.slurm` scripts they call and in ohc_ingest's `config.toml`. Run configs are stamped in the resulting .nc files for reference.
