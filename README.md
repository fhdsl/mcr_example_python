## How to Restore this project

1. Install uv on your machine
2. Clone this repo to your own machine using `git clone` or GitHub Desktop
3. Open in Positron / RStudio / VSCode
4. Run `uv sync` in terminal 
5. You may have to reopen the project to activate the environment for the notebook, or run `source .venv/bin/activate` in terminal
6. Open the `ipynb` file, make sure that the right kernel is open (should be Python 13.2 with the name of your environment, which should be "(mcr_python)")
7. Try running everything in the notebook!

## How I made this project

1. In Positron, I made a new folder from template, using the python Template
2. Run `uv init` in terminal
3. Add packages using `uv add <package>` such as `uv add geopandas`
4. `git init` to initialize a git repo
5. `git add .` and `git commit -m "starting"`
6. Publish to a remote using GitHub Desktop Publish.

## If you're in the middle of an analysis

If you are the in the middle of analysis, you might not have had the chance to use `uv`, or you just learned about it. There is a path to making your analysis reproducible:

1. Using `pip freeze > requirements.txt` will get you part of the way there, 
2. Or in your notebook use:

```python
session_info.show(na=True, os=True, cpu=False, jupyter=None, 
    dependencies=None,  write_req_file=True, 
    req_file_name="requirements.txt") 
```

using the `session-info` package (note that the package name is a hyphen, not an underscore, and module uses an underscore). This will create a `requirements.txt` file in your folder.

3. Run `uv init` in terminal, which will create your `uv.lock` and your `.venv` directory. 
4. Run `uv add -r requirements.txt` - this will install everything and modify your `uv.lock` file
5. `git add .` and `git commit`. Push to GitHub using Github Desktop.
6. Test it out by cloning and using the process above.

## Making The Project Binder Ready

- I used the `quarto use binder` command after making this a quarto project using `quarto create project`, then committed everything.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fhdsl/mcr_example_python/HEAD)
