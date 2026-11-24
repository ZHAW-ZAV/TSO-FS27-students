# TSO-FS27 — student exercises and examples

Traffic System Operations, spring semester 2027.
Currently released: **Python basics and Python visualization**. This collection
contains worked examples, unfinished exercises and their required historical data.
Further topics and solutions will be released as the semester progresses.

## Released course material

| Topic | Examples | Exercises |
|---|---|---|
| `01_python_basics` | Python, NumPy, pandas introductions | CO2 emissions; European airports |
| `02_python_viz` | Plotly introduction with Matplotlib comparison | Flight trajectories; CO2 visualization |

The current release contains **8 notebooks: 4 examples and 4 exercises**.
Your exercise tasks remain unfinished, with their explanations and scaffolding
provided. Exercise notebooks start without saved outputs; work through the tasks
in order. Worked-example code and outputs are supplied for reference.

## Local setup

Use Python 3.13 and [uv](https://docs.astral.sh/uv/getting-started/installation/).
From this checkout, run:

```sh
uv sync --locked
```

Select `.venv` as your notebook kernel in your IDE. The interpreter is
`.venv/bin/python` on macOS/Linux and `.venv/Scripts/python.exe` on Windows.
Run each notebook from its topic directory so relative data paths resolve.
The shared course environment is provided now and will also support later topics;
there are no separate topic environments or instructor preparation dependencies.

For PNG/PDF export, Kaleido also requires Chrome/Chromium. If it is not installed:

```sh
uv run --locked python -c "import plotly.io as pio; pio.get_chrome()"
```

`BROWSER_PATH` can select an existing compatible browser. Generated figures go to
local `figures/` folders and are ignored. Map background tiles require internet access.

## Google Colab

Each notebook's badge opens its path in
[ZHAW-ZAV/TSO-FS27-students](https://github.com/ZHAW-ZAV/TSO-FS27-students), branch `main`.
Opening a notebook does not automatically copy every repository file into the
Colab runtime. Run its setup cell; the supplied loaders reuse local files and
obtain missing inputs as explained in the notebook. Repeat setup after a runtime
reset. The local Python 3.13 lock and Colab runtime setup are separate workflows.

## Data and generated outputs

Required snapshots are included unchanged alongside the released lessons. Data
years are historical and do not need to match the course year. Iris is supplied by
the plotting library where the example specifies it. No live data preparation is
required. The supplied airport counts include the types documented in the exercise;
check country mappings and population coverage as instructed. Capitals are display
anchors for country totals, not the locations of aviation emissions.

`pyproject.toml` defines teaching dependencies and `uv.lock` fixes the resolution.
`requirements.txt` is a generated pip compatibility export, not another version
list to maintain. Do not edit its package pins by hand. After updating your local
course copy with `git pull`, run `uv sync --locked` again.
