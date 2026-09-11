# IIT414W - Lab 0: Reproducible Setup

## Environment

- Python version: 3.12.10
- Kernel: Python (IIT414W)
- Course seed: 414
- Operating system: Windows

## Setup

Create a virtual environment:

```powershell
py -3.12 -m venv .venv
```

Activate the virtual environment:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install the required packages:

```powershell
python -m pip install -r requirements.txt
```

Register the Jupyter kernel:

```powershell
python -m ipykernel install --user --name iit414w --display-name "Python (IIT414W)"
```

## Notebook order

Run the notebooks in this order:

1. `unit_I/week_01/W01_Thu_setup_and_reproducibility_v2.ipynb`
2. `unit_I/week_01/W01_Fri_f1_data_ecosystem_v1.ipynb`

For the final verification, I restarted the kernel and ran all cells in each notebook.

## Friday data route

The Friday notebook was executed with:

```python
MODE = "snapshot"
```

Both tables used the course-provided real-data snapshot for the 2021 Italian Grand Prix.

- Results source: `PROVIDED_SNAPSHOT`
- Laps source: `PROVIDED_SNAPSHOT`

This is a stored verified copy of real race data. It does not prove that a live API request was made.

## Outputs

Thursday setup evidence is saved in:

`outputs/setup_evidence_20260911T004307_960047Z.json`

Friday evidence is saved in:

`outputs/w01_fri_20260911T012451_822316Z_569888/`

The Friday output folder contains the exported results, laps, checks and `run_manifest.json`.

## Evidence notes

### Source

The event used was the 2021 Italian Grand Prix.

One row in the results table represents one driver's final result in the race.

One row in the lap table represents one lap completed by one driver. A driver can appear many times because each driver completes multiple laps.

Both tables were supplied by `PROVIDED_SNAPSHOT`, which is a stored copy of real race data and not synthetic teaching data.

### Check

I ran an independent check for missing driver numbers in the lap table.

Observed result:

`Missing driver numbers: 0`

This establishes that every lap row in this dataset has a driver number recorded.

It does not prove that every driver number is correct or that the entire dataset is complete.

### Decision and verification

I used the provided snapshot route because it is reproducible and is an accepted real-data route for Lab 0.

I verified the decision by checking the notebook source labels. Both the results table and lap table reported `PROVIDED_SNAPSHOT`.

I also kept the course seed at 414 and verified that the Thursday reproducibility check passed.

## Repository

Repository link: https://github.com/cote8/Lab0-Entrega

Submitted commit ID: c655ca8