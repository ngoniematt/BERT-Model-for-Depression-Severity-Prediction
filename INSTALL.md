# Install notes

## Option A — portable (CPU/generic)
```bash
python -m venv .venv && source .venv/bin/activate  # (Windows: .venv\Scripts\activate)
pip install --upgrade pip
pip install -r requirements.txt
```

## Option B — GPU (CUDA 12.1)
```bash
python -m venv .venv && source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements-cu121.txt
```

If you have a different CUDA (e.g., cu118), change the index URL to:
`--extra-index-url https://download.pytorch.org/whl/cu118`
and replace the `+cu121` suffix with `+cu118` on the torch packages.
