# Pipenv Test Case 7: pyproject.toml Fallback

## What This Tests
Tests detection of Python version from pyproject.toml when no higher-priority files specify a version.

## Expected
>=3.8 found through PyprojectTomlRequiresPython

## Files
- `Pipfile` - No requires section
- `pyproject.toml` - Contains `requires-python = ">=3.8"`

## Expected Behavior
Your version detection tool should detect **Python >=3.8** from pyproject.toml.

## Priority
This is the **fifth priority** detection method for Pipenv projects (after .python-version, .tool-versions, Pipfile, and Pipfile.lock).

## Note
pyproject.toml serves as a fallback when Pipenv-specific files don't specify a Python version.
