# COMPAS package template for C++/Python binding 

Cookiecutter template for COMPAS C++ based extensions.

[Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/readme.html#)
is a command-line utility that lets you quickly bootstrap a new project from a template.
It takes a directory tree and copies it into your new project,
replacing all the generic info that finds surrounded by templating tags `{{` and `}}` with your project info written in `cookiecutter.json`.

## Features

* Project directory and file structure
* Documentation based on [Sphinx](http://www.sphinx-doc.org/en/master/)/[reStructuredText](http://docutils.sourceforge.net/rst.html)
* Testing framework: [pytest](https://docs.pytest.org/en/latest/)
* Basic setup script to create pip installable packages
* Automation of common tasks for development workflow based on [pyinvoke](http://www.pyinvoke.org/) (generate documentation, run tests, check format, etc.)
* [EditorConfig](https://editorconfig.org/) integration
* Minimal Github workflows for CI/CD
* Example project for [nanobind](https://github.com/wjakob/nanobind)
* Python wheel building via [cibuildwheel](https://github.com/pypa/cibuildwheel) and [scikit-build-core](https://github.com/scikit-build/scikit-build-core) for [PyPI](https://pypi.org/).

## What's included

* `.github`
* `data`
* `docs`
* `scripts`
* `src`
* `temp`
* `tests`
* `.editorconfig`
* `.gitignore`
* `CHANGELOG.md`
* `CONTRIBUTING.md`
* `LICENSE`
* `pyproject.toml`
* `README.md`
* `requirements-dev.txt`
* `requirements.txt`
* `tasks.py`

## Requirements

Install the `cookiecutter` command line utility: `pip install cookiecutter`.

## Usage

In the terminal, go to the folder where you want to place your project:

```bash
cd <your-projects-folder>
```

Generate a new Cookiecutter template layout:

```bash
cookiecutter gh:compas-dev/compas_package_template
```

Go to project folder:

```bash
cd <project-slug>
```

Add the project files to the new `git` repo:

```bash
git add .
git commit -m "Initial commit"
```

[Detailed instructions](https://docs.google.com/presentation/d/1HL4o8cadvuZlQDsdYlslzeDhDVvTUlPdk9zTSn5fsLA/edit?slide=id.g9da5d6f0fe_0_0#slide=id.g9da5d6f0fe_0_0)

## Additional settings

To use the coding style feature with [EditorConfig](https://editorconfig.org/):

Some text editors have a native EditorConfig.
If yours doesn't, you can download the appropriate plugin [here](https://editorconfig.org/#download).

## Github Actions

Basic CI/CD has already been setup in the .github folder, including automatic building and testing across systems, documentation generation etc.

### Automatic Publishing to PYPI

This requires adding your PYPI token in the repo or organization secrets as `PYPI`.
If you don't need this feature, go to [.github/workflows/release.yaml]({{cookiecutter.project_folder}}/.github/workflows/release.yml) and delete lines 95-99.
By default the package is uploaded to test.pypi.org. For publishing to pypi.org delete lines 97-99.

## License

This template is licensed under the terms of the [MIT License](/LICENSE).
