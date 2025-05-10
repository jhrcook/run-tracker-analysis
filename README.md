# Analysis of my runs

```bash
uv pip compile -q -o requirements.out requirements.in
uv pip install -r requirements.out
```

```bash
jupyter nbconvert --inplace --execute analysis.ipynb && \
    jupyter nbconvert --to html analysis.ipynb && \
    nb-clean clean analysis.ipynb
```
