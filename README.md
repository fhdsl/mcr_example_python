## How to Restore this project

1. Install uv on your machine
2. Clone this repo to your own machine using `git clone` or GitHub Desktop
3. Open in Positron / RStudio / VSCode
4. Run `uv sync` in terminal 
5. You may have to reopen the project to activate the environment for the notebook, or run `source .venv/bin/activate` in terminal
6. Open the `ipynb` file, make sure that the right kernel is open (should be Python 13.2 with the name of your environment)
7. Try running everything!

## How I made this project

1. In Positron, I made a new folder from template, using the python Template
2. Run `uv init` in terminal
3. Add packages using `uv add <package>` such as `uv add geopandas`
4. `git init` to initialize a git repo
5. `git add .` and `git commit -m "starting"`
6. Publish to a remote using GitHub Publish.

## Making The Project Binder Ready


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fhdsl/mcr_example_python/HEAD)
