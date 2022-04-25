# Pylint Rules

This project contains my default rcfile for [pylint](https://pylint.pycqa.org/en/latest/) code style checker.

## Usage

copy to your project in the root

```shell
pylint src/ tests/ --rcfile .pylintrc
```

or use directly from url

```makefile
codestyle:
	@RCFILE=$(shell mktemp) && \
	wget -q 'https://raw.githubusercontent.com/vitalibo/pylint-rules/master/.pylintrc' -O $$RCFILE && \
	pylint src/ tests/ --rcfile $$RCFILE && \
	rm -rf $$RCFILE
```
