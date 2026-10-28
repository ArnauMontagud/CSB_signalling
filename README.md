# CSB signalling practical

Hands-on material on Boolean modelling of signalling networks for
**Computational Systems Biology** (42589), Master's in Bioinformatics, ETSE,
Universitat de Valencia. Sessions 8 and 9.

## Run it in your browser

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ArnauMontagud/CSB_signalling/HEAD?urlpath=lab/tree/practical_signalling.ipynb)

Click the badge. There is nothing to install and nothing to download. The first
launch of the day can take a few minutes while the environment is prepared, after
that it takes about half a minute.

Two things to know before you start:

1. **Binder keeps nothing.** When your session ends, everything you typed is gone.
   Save a copy on your computer with `File > Download` as soon as you start working,
   and again at the end: the notebook you download is the one you hand in.
2. **Ten minutes without activity closes the session.** If you leave for the break,
   download your notebook first and relaunch when you come back.

## What is in here

| File | What it is |
|---|---|
| `practical_signalling.ipynb` | The notebook we use in class, with hands-on 1 to 3 and tasks 1 to 3 |
| `models/Metastasis_Master_Model.zginml` | Metastasis model, the worked example |
| `models/PKN.zginml` | Prostate cancer model, used in the tasks |
| `binder/Dockerfile` | The environment Binder builds, pinned to a tested CoLoMoTo image |
| `environment.yml` | The exact software versions, for installing locally |
| `INSTALL.md` | How to run everything on your own machine instead |

## Tools

- [GINsim](https://ginsim.github.io/) for loading and visualising logical models
- [bioLQM](https://colomoto.github.io/bioLQM/) for attractor analysis
- [MaBoSS](https://maboss.curie.fr/) for stochastic simulation of Boolean models
- All of them through the [CoLoMoTo](http://colomoto.org/) notebook environment

## If Binder does not work

Binder is a free community service and it does go down. In order:

1. Wait two minutes and retry the badge. Most failures are a build that is still running.
2. Try the direct link without the notebook path:
   `https://mybinder.org/v2/gh/ArnauMontagud/CSB_signalling/HEAD`
3. Install locally following `INSTALL.md`. It takes about 15 minutes on a good connection.

## Previous editions

Each edition is kept as a git tag, so the material as delivered that year can
always be recovered and relaunched:

- 2025-26: `https://mybinder.org/v2/gh/ArnauMontagud/CSB_signalling/2025-26`

## Credits

Adapted from Noel V, Naldi A, Calzone L, Pauleve L, Thieffry D (2025),
"Reproducible Boolean model analyses and simulations with the CoLoMoTo software
suite: a tutorial", *Interface Focus* 15: 20250002,
[doi:10.1098/rsfs.2025.0002](http://doi.org/10.1098/rsfs.2025.0002).
Original notebook: [10.5281/zenodo.15602428](https://dx.doi.org/10.5281/zenodo.15602428).

Adapted for this course by Arnau Montagud (I2SysBio, CSIC-UV).
