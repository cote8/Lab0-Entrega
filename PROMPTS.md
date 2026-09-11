# AI Use Record - Lab 0

## Tool

- Tool: ChatGPT
- Model: GPT-5.6 Sol

## Purpose

I used ChatGPT as technical support while completing Lab 0.

The assistance included:

- understanding the Thursday and Friday notebook instructions;
- configuring the Python 3.12 virtual environment and Jupyter kernel;
- troubleshooting Git, Jupyter and package installation;
- understanding the difference between the results-table grain and lap-table grain;
- interpreting `PROVIDED_SNAPSHOT`, `JOLPICA_HTTP`, `FASTF1_SESSION` and synthetic data;
- designing a simple independent data check;
- understanding why post-race fields such as `position` cannot be used as pre-race features;
- reviewing the structure required for the Lab 0 README and submission package.

## Meaningful assistance used

I used the suggested setup steps to create a Python 3.12 virtual environment and install the course dependencies.

I also used explanations from ChatGPT to help write and understand my notebook responses. I did not treat the suggestions as execution evidence; I ran the notebooks and checked the outputs myself.

For the Friday notebook, I used an independent check that counted missing values in `driver_number`:

`laps["driver_number"].isna().sum()`

My observed result was:

`Missing driver numbers: 0`

I also used the explanation that `grid` can be known before the race, while final `position` is only known after the race and would cause data leakage if used for a pre-race prediction.

## Verification

I verified the technical assistance using my own notebook outputs.

The Thursday notebook showed:

- Python 3.12.10
- Git available
- seed 414 reproducibility check passed
- course root marker found
- technical status `READY`
- setup evidence saved successfully

The Friday notebook showed:

- `MODE = "snapshot"`
- Results source: `PROVIDED_SNAPSHOT`
- Laps source: `PROVIDED_SNAPSHOT`
- Independent check result: 0 missing driver numbers
- final evidence exported with `run_manifest.json`

I restarted the kernel and ran all cells in both notebooks before keeping the final outputs.

## Limitations

ChatGPT helped with explanations and troubleshooting, but it did not replace my own execution of the notebooks.

The AI suggestions alone do not prove that my environment works, that the data are correct, or that live API access succeeded. I verified the relevant claims using the outputs produced on my own computer.