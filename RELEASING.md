# Releasing NeoCore

## 1) Prepare
- Ensure CI is green on `main`.
- Update `CHANGELOG.md`.
- Bump `neocore/__init__.py::__version__` and `pyproject.toml::project.version`.

## 2) Tag and GitHub release
```bash
git checkout main
git pull --ff-only
git tag vX.Y.Z
git push origin vX.Y.Z
```
Create a GitHub Release titled `vX.Y.Z` and paste release notes from changelog.

## 3) Publish to PyPI (when ready)
```bash
python -m pip install --upgrade build twine
python -m build
python -m twine upload dist/*
```

## 4) Verify
- `pip install neocore==X.Y.Z`
- `python -m neocore.scenarios.payment_rail`
