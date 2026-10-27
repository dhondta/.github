# Contributing

Thank you for your interest in contributing! These guidelines apply to every repository of [dhondta](https://github.com/dhondta) that does not define its own `CONTRIBUTING.md`. Projects with a documentation site may also have a *Contributing* page with project-specific details.

By participating, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md).

## Asking questions

Before opening an issue, check the project's documentation (linked from its README). Questions about usage are welcome as issues.

## Reporting issues

Open an issue in the relevant repository and use the matching template. Please include:

- the project version (`--help` of the command-line tools usually prints it) and your Python version and OS;
- the exact command and its full output (traceback included), ideally in verbose mode;
- if relevant, the input that triggers the issue (or a link to it).

Archived repositories are no longer maintained and do not accept issues.

## Security

Please do **not** report vulnerabilities in public issues. See the [security policy](SECURITY.md): report them privately through the affected repository's *Security* tab (*Report a vulnerability*).

## Pull requests

1. Fork the repository and create your branch from `main`.
2. Keep the change focused: one feature or fix per pull request.
3. Follow the style of the surrounding code. The Python projects are linted with [flake8](https://flake8.pycqa.org/) (lines up to 127 characters) and tested with [pytest](https://docs.pytest.org/):
   ```console
   $ pip install -e .
   $ pip install flake8 pytest pytest-cov
   $ flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics
   $ pytest
   ```
4. Add or update the tests and the documentation.
5. Open the pull request and fill in its template. The CI must pass.

## Releasing (maintainer)

The version of a Python package is stored in its `VERSION.txt`. On every push to `main`, the CI checks whether this version is already on PyPI. If not, it builds the package and publishes it. Bumping `VERSION.txt` is thus all it takes to release.

## Documentation

The documentation of each project is an [MkDocs](https://www.mkdocs.org/) site (Material theme) built by [Read the Docs](https://readthedocs.org/) from `docs/`:

```console
$ pip install -r docs/requirements.txt
$ mkdocs serve -f docs/mkdocs.yml          # live preview at http://127.0.0.1:8000
$ mkdocs build --strict -f docs/mkdocs.yml # what Read the Docs runs
```
