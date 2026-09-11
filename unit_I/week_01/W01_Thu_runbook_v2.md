# W01 Thu - Setup and reproducibility runbook

Use this runbook with `W01_Thu_setup_and_reproducibility_v2.ipynb` during the technical studio on Thursday 3 September. The notebook supports the 45-minute setup block; peer verification follows for 10 minutes. It does not replace the separate exit ticket or Lab 0.

No Formula 1 knowledge is needed for this technical block. The timing table is a fictional execution check, not race data or a sports question. Read the written steps before running code. The times are guidance, not deadlines, and you may pause to ask for a step to be restated.

## Quick glossary

- **Seed:** a starting value that makes a pseudo-random procedure repeatable when code and inputs stay the same.
- **Kernel:** the running Python process that executes a notebook cell.
- **Dependency:** a software package that code needs.
- **Project path:** the folder location used to find and save project files.
- **Reproducibility:** another person can repeat a documented procedure and inspect the same kind of evidence.

## Your route

| Block | What and how | Materials / time | Expected evidence |
| --- | --- | --- | --- |
| Plan your check | Write a success check and a possible failure before running code. | Notebook; 5 min. | Your own check, risk, and first response. |
| Health check | Run the Python, kernel, Git, and package cells in order. Read every message. | Jupyter notebook; 10 min. No installation. | Actual versions and status messages. |
| Seed and offline example | Run the synthetic timing-table cell and compare its two runs. | Python standard library; 10 min. | A table and a PASS or FAIL comparison. |
| Save and reproduce | Find `.iit414w-root`, then save evidence after recording your result. | Course project folder; 10 min. | A new JSON file under `outputs/`. |
| Record and verify | Record your own status, limitation, and next action; then restart and run all. | Your observed results; 10 min. | Ready, Minor fix, or Blocked plus next action. |

## Minimum environment

The setup block checks Python 3.10 or later, a Jupyter kernel that can execute the notebook, Git, `RANDOM_SEED = 414`, and a verified project root.

The main route is offline and uses only the Python standard library. The notebook reports the availability of NumPy, pandas, requests, and FastF1 without importing them before the check. It does not install packages, call web APIs, inspect Git history, read credentials, or modify your PATH.

## Run the notebook

1. Complete the planning notes, then run the health-check cells in order.
2. Read the synthetic-table labels and run the seed cell. Matching outputs show a repeatable small procedure, not complete reproducibility.
3. Run the project-root cell. If the marker is not found, stop and follow its written next action; do not make a new project folder.
4. Record one additional check, your real status, one limitation, and your next action. The optional code cell only saves status text you enter yourself. Blank text remains `NOT RECORDED`.
5. Run the evidence cell. It creates a new timestamped file such as `outputs/setup_evidence_YYYYMMDDTHHMMSS_microsecondsZ.json`; it never overwrites an existing file.
6. Save the notebook, then use **Restart Kernel and Run All**. A kernel running once is not evidence of a restart.

If a step is unclear, ask a facilitator or partner to restate the task. Do not ask another person to enter your result or select your status.

## Common failures

| Message or situation | Meaning | First next action |
| --- | --- | --- |
| `[FAIL] Python 3.10+` | The selected interpreter is too old. | Install or activate Python 3.10+ and select it as the notebook kernel. |
| `[NOT CHECKED] Jupyter kernel` | This file is not running in a Jupyter notebook kernel. | Open it in Jupyter/JupyterLab, select a Python kernel, and run again. |
| `[FAIL] Git available` | `git --version` did not run successfully. | Install Git, restart Jupyter, and rerun the health check. Do not paste credentials into the notebook. |
| `MISSING` for a Friday package | A later-session package is not present. | Record it as a preparation task; ask for support before Friday. Do not add automatic installation commands to this notebook. |
| Project root marker not found | The notebook was opened outside the course project or in an unrelated copy. | Open the project folder containing `.iit414w-root`, or one of its subfolders, then rerun the root cell. |
| Evidence was not saved | Earlier cells were skipped, the root was not found, or the output directory was unavailable. | Run the technical cells in order and read the exact status message. |

If Python or Jupyter cannot start, do not claim that your machine is ready because a classmate's computer worked. Record the block and the support you need in the exit ticket.

## Peer verification and next steps

Keep the newest evidence file. During the 10-minute verification, a peer may inspect what you produced and ask about it, but your work and status remain your own. Carry your actual status and next action to the existing exit ticket.

Friday's F1 data ecosystem session has a separate notebook and setup needs. Resolve missing preparation packages with course support before then. Use the current course programme and calendar for published assessment details; this runbook does not create a submission or a new deadline.
