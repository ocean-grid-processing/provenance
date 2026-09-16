# provenance
provenance records for OHC pipeline runs.

## 260908-OP20260507

First production run; data released as https://doi.org/10.5281/zenodo.22757913.

- Input: LocalGP [run OP20260507](https://github.com/argovis/ocean_pipeline/tree/main/provenance/localGP#op20260507-series)
- Pipeline code:
  - ohc_ingest: https://github.com/ocean-grid-processing/localgp_ohc_ingest/releases/tag/1.0.0
  - ohc_derive: https://github.com/ocean-grid-processing/ohc_derive/releases/tag/1.0.0
  - ohc_ohca_ohu_emitter: https://github.com/ocean-grid-processing/ohc_ohca_ohu_emitter/releases/tag/1.0.0
  - ohc_gcos_emitter: https://github.com/ocean-grid-processing/ohc_gcos_emitter/releases/tag/1.0.0
  - ohc_map_emitter: https://github.com/ocean-grid-processing/ohc_map_emitter/releases/tag/1.0.0
- Pipeline environment: https://github.com/ocean-grid-processing/provenance/blob/main/environments/ohc_crosscheck
- Runbook notes: each pipeline step has a `run.sh` to manage slurm scheduling on CU Blanca; set parameters therein, as well as in the top-level `.slurm` scripts they call and in ohc_ingest's `config.toml`. Run configs are stamped in the resulting .nc files for reference.
