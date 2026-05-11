# Python for AI Students

A condensed, modular Python curriculum designed for AI students. Three modules covering Python foundations through data analysis and visualization.

## Course Structure

| Module | Topics | Notebook | Reference PDF | Challenges |
|--------|--------|----------|---------------|------------|
| **Module 1** | Syntax, Variables, Types, Operators, Control Flow, Data Structures, Functions, Scope, List Comprehensions, Lambda | [Module_1_Python_Foundations.ipynb](modules/Module_1_Python_Foundations.ipynb) | [Module_1_Reference.pdf](modules/Module_1_Reference.pdf) | [Module_1_Challenges.ipynb](modules/Module_1_Challenges.ipynb) |
| **Module 2** | Classes, Inheritance, File I/O, Exceptions, NumPy Arrays, Slicing, Broadcasting | [Module_2_OOP_Files_NumPy.ipynb](modules/Module_2_OOP_Files_NumPy.ipynb) | [Module_2_Reference.pdf](modules/Module_2_Reference.pdf) | [Module_2_Challenges.ipynb](modules/Module_2_Challenges.ipynb) |
| **Module 3** | Pandas, Data Cleaning, Grouping, Matplotlib, End-to-End Mini-Project | [Module_3_Pandas_Matplotlib_MiniProject.ipynb](modules/Module_3_Pandas_Matplotlib_MiniProject.ipynb) | [Module_3_Reference.pdf](modules/Module_3_Reference.pdf) | [Module_3_Challenges.ipynb](modules/Module_3_Challenges.ipynb) |

## Data

Sample datasets for Module 3 exercises and mini-project:

- [data/students.csv](data/students.csv) - 50 student records with GPA, attendance, department
- [data/sales.csv](data/sales.csv) - 100 sales transactions across categories and regions

## Resources

### Official Documentation
- [Python.org Downloads](https://www.python.org/downloads/)
- [Python 3 Documentation](https://docs.python.org/3/)
- [Python Tutorial](https://docs.python.org/3/tutorial/)

### Tutorials
- [After Hours Programming - Python](https://afterhoursprogramming.com/tutorials/python)
- [Learn Python in 10 Minutes](https://stavros.io/tutorials/python/)
- [Python for Scientists](https://nbviewer.org/gist/rpmuller/5920182)
- [Python Beginners Guide](https://wiki.python.org/moin/BeginnersGuide)

### Interactive Tools
- [Python Tutor](https://pythontutor.com/) - Visualize code execution step by step
- [Replit](https://replit.com/) - Online Python editor

### Arabic Resources
- [Python Arabic Language Resources](https://wiki.python.org/moin/ArabicLanguage.html)

## Setup (Using `uv`)

This project uses [`uv`](https://docs.astral.sh/uv/) for fast Python package management and virtual environments.

### 1. Install `uv`

**macOS / Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows:**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

For other methods (pip, Homebrew, etc.), see the [official uv installation guide](https://docs.astral.sh/uv/getting-started/installation/).

### 2. Create a Virtual Environment

From the project root (where this `README.md` is):
```bash
uv venv --python 3.14
```

This creates a `.venv/` directory with a self-contained Python interpreter.

### 3. Install Dependencies

```bash
uv pip install numpy pandas matplotlib scikit-learn nbconvert nbformat ipykernel
```

**What each package is for:**
| Package | Purpose |
|---------|---------|
| `numpy` | Numerical computing (arrays, matrices, math operations) |
| `pandas` | Data manipulation and analysis (DataFrames) |
| `matplotlib` | Data visualization and plotting |
| `scikit-learn` | Machine learning utilities (used in Regression Exercise) |
| `nbconvert` | Convert notebooks to other formats |
| `nbformat` | Read/write Jupyter notebook files |
| `ipykernel` | Jupyter kernel for running notebooks in VS Code/Jupyter |

### 4. Register the Jupyter Kernel

So VS Code and Jupyter can find this environment:
```bash
.venv/bin/python -m ipykernel install --user --name ec-ai-python
```

> **Windows users:** Use `.venv\Scripts\python -m ipykernel install --user --name ec-ai-python`

Then in VS Code, click the kernel selector (top-right of a notebook) and choose **"ec-ai-python"**.

### 5. Verify Everything Works

Run the notebooks from the `modules/` directory in VS Code or Jupyter. The data files are referenced as `../data/...` (relative to the `modules/` folder).

---

## How to Use

1. Open the notebooks in Jupyter, VS Code, or Google Colab
2. Each module notebook covers concepts with examples and exercises
3. Each challenges notebook contains programming problems for practice
4. Reference the PDF documents for detailed concept explanations
5. Module 3 uses the provided CSV files in the `data/` directory

## Credits

Curriculum designed for the EC AI Student Course. Based on the After Hours Programming Python tutorial and supplemented with modern Python practices.
