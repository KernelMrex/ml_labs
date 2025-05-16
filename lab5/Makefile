VENV_DIR := .venv
PYTHON := python3.13
VENV_PY := $(VENV_DIR)/bin/python
VENV_PIP := $(VENV_DIR)/bin/pip

.PHONY: all venv install-jupyter clean

# Default target
all: venv install-jupyter

# Create virtual environment
venv:
	$(PYTHON) -m venv $(VENV_DIR)
	$(VENV_PIP) install --upgrade pip

# Install Jupyter and register kernel
install-jupyter:
	$(VENV_PIP) install notebook jupyterlab ipykernel
	$(VENV_PY) -m ipykernel install --user --name=lab5 --display-name "Python (lab5)"

# Remove venv
clean:
	rm -rf $(VENV_DIR)
