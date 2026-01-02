<!-- file: README.md -->
<!-- version: 1.0.0 -->
<!-- guid: 3e7a9f2d-4c8b-5e1a-8d6f-1c9e4a2b7d3e -->

# Release Python Package Action

Build and publish Python packages to PyPI with automated testing and validation.

## Features

- 🐍 Python 3.13+ support
- 📦 Multiple build backends (setuptools, poetry, hatchling)
- ✅ Automated testing before publish
- 🔍 Metadata verification
- 🚀 PyPI and TestPyPI support

## Usage

```yaml
- uses: jdfalk/release-python-action@v1
  with:
    pypi-token: ${{ secrets.PYPI_TOKEN }}
```

## Inputs

| Input             | Description       | Required | Default         |
| ----------------- | ----------------- | -------- | --------------- |
| `python-version`  | Python version    | No       | `3.13`          |
| `package-dir`     | Package directory | No       | `.`             |
| `build-backend`   | Build backend     | No       | `setuptools`    |
| `run-tests`       | Run tests         | No       | `true`          |
| `test-command`    | Test command      | No       | `pytest`        |
| `repository-url`  | PyPI URL          | No       | PyPI production |
| `pypi-token`      | PyPI token        | Yes      | -               |
| `skip-existing`   | Skip existing     | No       | `false`         |
| `verify-metadata` | Verify metadata   | No       | `true`          |

## License

MIT
