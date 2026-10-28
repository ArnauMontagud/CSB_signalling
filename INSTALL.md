# Running the practical on your own machine

You do not need this for the class: the Binder link in the README gives you the
same environment in your browser. Use this if you want to keep the models and
results on your own machine, or if Binder is down.

Allow about 15 minutes and 10 GB of free disk space.

## 1. Get conda

- **Windows**: install WSL first (`wsl --install` in PowerShell as administrator,
  then reboot), and do everything below inside the Ubuntu terminal. Installing
  conda in Windows directly also works but the CoLoMoTo packages are better tested
  on Linux.
- **Linux and WSL**:

  ```bash
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
  bash Miniconda3-latest-Linux-x86_64.sh
  ```

- **macOS**: download the installer for your CPU (Apple silicon or Intel) from
  <https://repo.anaconda.com/miniconda/> and run it with `bash`.

Close and reopen the terminal when the installer finishes.

## 2. Create the environment

From the folder where you cloned or unzipped this repository:

```bash
conda env create -f environment.yml
conda activate CSB
```

The versions in `environment.yml` are pinned on purpose. If you install the
packages by hand without the pins you will very likely get a GINsim build in
which the bioLQM tools (`biolqm.fixpoints` and friends) are missing, and the
notebook will fail halfway through.

## 3. Launch the notebook

```bash
jupyter lab practical_signalling.ipynb
```

## Problems seen in previous years

| Symptom | Fix |
|---|---|
| `biolqm.fixpoints` does not exist, or `AttributeError` on a bioLQM function | You are not using the pinned `ginsim=3.0.0b`. Recreate the environment from `environment.yml` |
| Error mentioning `libc6` or `GLIBC` when running MaBoSS on WSL | `sudo apt install glibc-source` |
| `java: command not found` or GINsim fails to start | The environment ships its own Java. Make sure you ran `conda activate CSB` in the same terminal |
| Conda takes forever to solve | Use `conda env create -f environment.yml --solver=libmamba`, or install `mamba` and use `mamba env create` |
| `ginsim.show()` shows nothing | `conda install -c conda-forge graphviz pygraphviz` inside the environment |

## Optional: the GINsim desktop application

The practical does not need it, everything is done from the notebook. If you want
to draw and edit models with a mouse, download the standalone application from
<https://ginsim.github.io/install/>. It needs Java installed on your system.
