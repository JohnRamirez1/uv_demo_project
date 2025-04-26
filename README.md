# UV project

📦 uv Guide: Fast Package and Project Management
uv is a next-generation Python package manager and project manager designed for speed, reliability, and modern workflows.
It combines the best of tools like pip, pip-tools, and virtualenv — but faster and easier to use.

Whether you're building cutting-edge LLM (Large Language Model) applications, managing complex dependency trees, or preparing libraries for PyPI publication, uv helps you work smarter.

✨ Why Use uv?
🚀 Blazing Fast: Installs and resolves dependencies up to 10x faster than traditional tools.

🎯 Predictable Environments: Lock dependencies exactly, critical for reproducibility in AI/LLM experiments.

📦 Seamless Publishing: Makes preparing and publishing Python packages to PyPI simple and clean.

🧠 Perfect for LLM Projects: Ensures deterministic builds and isolates environments, which is vital for consistency in AI training and inference.

In LLM projects, minor environment inconsistencies can cause huge model behavior differences.
uv guarantees that every install is exactly the same — across your dev machines, cloud servers, and CI/CD pipelines.


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