# IPSP Lab 4: Circuit Tuning

This repository contains the material for Laboratory 4 of the Integrated Photonics Systems and Projects (IPSP) course. The notebook models thermal phase shifters, computes their temperature profiles and effective refractive indices with FEMWELL, and uses these results to tune Mach–Zehnder interferometers with GDSfactory and SAX.

## Requirements

- Git
- Python 3.12 (the required version is recorded in `.python-version`)
- [`uv`](https://docs.astral.sh/uv/getting-started/installation/), for creating the environment and installing the project dependencies
- Jupyter support, either through Visual Studio Code with the Jupyter extension or JupyterLab

Use a terminal available on your operating system (PowerShell on Windows, Terminal on macOS, or a shell on Linux).

## Get started

Clone the repository and enter its directory:

```bash
git clone https://github.com/cccanvas-upv/ipsp-lab4.git
cd ipsp-lab4
```

Install the project dependencies from the lock file:

```bash
uv sync
```

`uv` creates a local `.venv` environment and installs the pinned dependency set from `uv.lock`. If Python 3.12 is not already installed, `uv` can install it when needed; otherwise, install Python 3.12 first and run `uv sync` again.

The environment follows [Laboratory 3](https://github.com/cccanvas-upv/ipsp-lab3), including the FEMWELL, Tidy3D, and SAX extras from Gplugins.

## Open the notebook

### Visual Studio Code

1. Open the cloned `ipsp-lab4` folder in Visual Studio Code.
2. Install the Microsoft **Jupyter** extension if it is not already installed.
3. Open [`40_Circuit_Tuning.ipynb`](./40_Circuit_Tuning.ipynb).
4. Select the project environment as the notebook kernel. It should appear as `.venv` or `Python 3.12`. The kernel display name saved in the notebook comes from the author's environment; select your local project environment.
5. Run the cells from top to bottom and complete the exercises where indicated.

### JupyterLab

From the repository directory, launch JupyterLab using the project environment:

```bash
uv run --with jupyterlab jupyter lab
```

Then open `40_Circuit_Tuning.ipynb` in the browser tab that opens.

## Laboratory activities

- **LO1. Phase Shifter Model:** build a waveguide and metal heater, simulate the temperature profile and effective index as a function of current, and determine the waveguide length required for a pi phase shift.
- **LO2. Tuning Mach-Zehnder Interferometers:** extract a circuit netlist, define compact component models, and use the LO1 results to study the MZI response under different heater currents.

The notebook includes intentional placeholders (`...`) and model definitions for students to complete. Run the cells in order, completing each exercise before running the cells that depend on it.

## Repository contents

- [`40_Circuit_Tuning.ipynb`](./40_Circuit_Tuning.ipynb) — the supplied student notebook, preserved without modifications.
- [`pyproject.toml`](./pyproject.toml) and [`uv.lock`](./uv.lock) — project metadata and reproducible dependency definitions.
- [`.python-version`](./.python-version) — Python version used for the laboratory.
- [`.gitignore`](./.gitignore) — excludes generated Python files, virtual environments, and notebook checkpoints.
