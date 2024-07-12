# deptry-example

```
python -m venv venv
. ./venv/bin/activate
pip install -e .
pip install deptry
deptry -v .
```

Will result in:


```
Scanning 1 file...

pyproject.toml: DEP002 'asyncio' defined as a dependency but not used in the codebase
pyproject.toml: DEP002 'pathlib' defined as a dependency but not used in the codebase
Found 2 dependency issues.

For more information, see the documentation: https://deptry.com/
```

This is incorrect; asyncio is used in the codebase, but it's a standard library.