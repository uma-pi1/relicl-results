# RelICL results

Results behind the paper
[RelICL: Training-free Relational Learning with Tabular Foundation Models](https://arxiv.org/abs/2610.01725).
The code is in [uma-pi1/relicl](https://github.com/uma-pi1/relicl).

## Layout

The paths match the code repository, so this repository can be copied over a
clone of it (see its README).

- `paper/baselines.csv`: baseline numbers reported in the paper.
- `paper/relbench-stats/`: dataset and task statistics of RelBench.
- `paper/experiments/outputs/<stage>/<db>_<task>/`: RelICL runs. Each run holds
  `_RESULTS.yaml` with the metrics per split, `.hydra/config.yaml` with the
  full configuration and `trace.yaml` with the run's log. In an ensemble, each
  `member_NN/` is one member run.
- `paper/experiments/hpo-outputs/<db>_<task>/`: one Optuna study per task, with
  one `trial-N/` per trial, the test run of the best trial in `trial-N-test/`,
  and all trials ranked in `_ANALYSIS/`.
- `paper/experiments/early-fusion-*`: the OpenML experiment on row embeddings
  as input columns.
- `examples/rdblearn/*/results/`: the comparison with RDBLearn on constructed
  tasks.

## Citation

```bibtex
@misc{forbat2026relicltrainingfreerelationallearning,
      title={RelICL: Training-free Relational Learning with Tabular Foundation Models},
      author={Simon Forbat and Rainer Gemulla},
      year={2026},
      eprint={2610.01725},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2610.01725},
}
```
