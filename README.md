# Create project

Install UV

```{powershell}
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Init project uvdemo

```{bash}
uv init uvdemo
```

Install Multiple Python version 

```{bash}
uv python install 3.10 3.11 3.12
```

Create virtual environment

```{bash}
uv venv
```

Activate virtual environment

```{bash}
.venv\Scripts\activate
```

Add individual packages to virtual environment.
- this command will create uv.lock
```{bash}
uv add numpy
```

Add packages to virtual environment using requirements.txt
```{bash}
uv add -r requirements.txt
```

run main.py
```{bash}
uv run main.py
```

Calculate and save the versions I should install later
```{bash}
uv lock
```

Install dependencies in uv.lock
```{bash}
uv sync
```

## Build your package with uv build

```{bash}
uv build
```
By default, uv build will build the project in the current directory,
and place the built artifacts in a dist/ subdirectory.

## Publishing your package

```{bash}
uv publish
```