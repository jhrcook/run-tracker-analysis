# Analysis of my runs

```bash
uv venv -p 3.12.11
source .venv/bin/activate
uv pip compile -q -o requirements.out requirements.in
uv pip install -r requirements.out
```

```bash
source .venv/bin/activate
ruff check --fix analysis.ipynb && ruff format analysis.ipynb
jupyter nbconvert --inplace --execute analysis.ipynb && \
    jupyter nbconvert --to html analysis.ipynb && \
    jupyter nbconvert --to markdown analysis.ipynb && \
    nb-clean clean analysis.ipynb
```

TODO:

1. Add the above commands as `nox`.
2. pandera schema for input tables
