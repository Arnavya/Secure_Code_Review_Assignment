## Setup

Create and activate a virtual environment, then install dependencies:

```bash
python3 -m venv venv
source venv/bin/activate        
# Windows: venv\Scripts\activate
pip install -r requirements.txt
```

## Running the app

```bash
python app.py
```

The app starts on `http://127.0.0.1:5050`.

## Static analysis

Using [Semgrep](https://semgrep.dev/), added in
`requirements.txt` after setup. Scan results present
in `semgrep-results/` folder.



To reproduce the scan (with the virtual environment activated):

```bash
# Make sure the results folder exists
mkdir -p semgrep-results

# Human-readable output
semgrep scan --config auto --exclude venv . > semgrep-results/semgrep_results.txt 2>&1

# Machine-readable output (JSON)
semgrep scan --config auto --exclude venv --json . > semgrep-results/semgrep_results.json
```

