# 🐍 python-poetry-template

A lightweight, ready-to-use template for modern Python projects using [Poetry](https://python-poetry.org/).  
Ideal for quick prototyping, scripting projects, or laying the foundation for scalable applications.

---

## 📦 Features

- 📜 Clean and minimal `pyproject.toml` with Poetry
- 🛠 Script-based layout (`scripts/` folder)
- ✅ Pytest test setup under `tests/`
- 🔒 Dependency locking with `poetry.lock`
- 🧪 Coverage support via `pytest-cov`
- 🌱 Ideal starting point for new projects

---

## 🚦 Getting Started

### 1️⃣ Create Your Project from this Template

- Click the green **Use this template** button at the top of this repository page.
- Choose **Create a new repository** and name your project (e.g., `my-python-tool`).
- Clone your new repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_PROJECT_NAME.git
cd YOUR_PROJECT_NAME
```

* * *

### 2️⃣ Install Dependencies

Make sure Poetry is installed, then run:

```bash
poetry install
```

* * *

### 3️⃣ Run the Script

There are two ways to run the example script:

#### 🖱️ As a CLI command

Thanks to the `[tool.poetry.scripts]` section in `pyproject.toml`:

```bash
poetry run template-script
```

#### 🐍 Directly via Python

```bash
poetry run python scripts/template_script.py
```

* * *

### 4️⃣ Run Tests

```bash
poetry run pytest
```

With coverage:

```bash
poetry run pytest --cov=scripts
```

* * *

🗂 Project Structure
--------------------

```text
python-poetry-template/
├── LICENSE                   # License file (MIT by default)
├── pyproject.toml            # Poetry config and dependencies
├── poetry.lock               # Exact version locks for reproducibility
├── README.md                 # You're reading it
├── scripts/                  # Your Python scripts live here
│   ├── __init__.py
│   └── template_script.py
└── tests/                    # Pytest-based test suite
    ├── __init__.py
    └── test_example.py
```

* * *

🧪 Example Script
-----------------

```python
# scripts/template_script.py

def main():
    print("Hello from template script!")

if __name__ == "__main__":
    main()
```

Run it with:

```bash
poetry run python scripts/template_script.py
```

* * *

⚙️ Recommended Dev Tools
------------------------

You can optionally install common dev tools:

```bash
poetry add --group dev black flake8 isort mypy pre-commit
```

Then initialize `pre-commit`:

```bash
pre-commit install
```

* * *

📝 License
----------

This project is licensed under the **MIT License**.  
See [LICENSE](LICENSE) for details.

* * *

🤝 Contributing
---------------

Feel free to fork this template, open issues, or submit pull requests.

* * *

> Created with ❤️ by Asterios Raptis

