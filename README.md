[README.md](https://github.com/user-attachments/files/34232643/README.md)
# 🐼 Pandas Learning Notes

A hands-on, class-by-class collection of Jupyter notebooks covering the fundamentals of **Pandas**, Python's go-to library for data analysis and manipulation. Each notebook combines short explanations, worked examples, and a mini practice exercise.

## 📚 Contents

| Class | Notebook | Topics Covered |
|-------|----------|----------------|
| 1 | `Pandas_Class1.ipynb` | What is Pandas, installing/importing, Series vs DataFrame, creating them from lists, dicts and NumPy arrays, `.loc` basics |
| 2 | `Pandas_Class2.ipynb` | Inspecting data (`head`, `tail`, `info`, `shape`, `dtypes`), selecting rows/columns (`[]`, `.loc`, `.iloc`), index & columns, renaming, `set_index` / `reset_index` |
| 3 | `Pandas_class3.ipynb` | Data cleaning: missing values (`isna`, `dropna`, `fillna`), `astype`, `replace`, `drop`, duplicates (`duplicated`, `drop_duplicates`) |
| 4 | `pandas_class4.ipynb` | Boolean indexing, multi-condition filtering (`&`, `\|`, `~`), `query()`, string operations with `.str` |
| 5 | `Pandas_Class5.ipynb` | Sorting (`sort_values`, `sort_index`), descriptive statistics (`mean`, `median`, `mode`, `std`, `describe`), `value_counts`, `corr`, `cov` |
| 6 | `Pandas_class6.ipynb` | Split–apply–combine, `groupby`, `agg`, `pivot_table`, `crosstab`, binning with `pd.cut` |
| 7 | `Pandas_class7.ipynb` | `concat` (vertical/horizontal), `merge` (inner/left/right/outer), `join` with index alignment, analyzing missing values after joins |
| 8 | `Pandas_class8.ipynb` | Time series: `pd.to_datetime`, datetime index, `resample` (daily/weekly/monthly/yearly) |

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- Jupyter Notebook / JupyterLab, or Google Colab

### Installation

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
pip install pandas numpy jupyter
```

### Run the notebooks

```bash
jupyter notebook
```

Then open any `.ipynb` file. Several notebooks were also run on Google Colab, so you can upload them there too.

## 🧠 Quick Reference

```python
import pandas as pd

# Create
df = pd.DataFrame({"Name": ["Alice", "Bob"], "Score": [88, 92]})

# Inspect
df.head(); df.info(); df.shape

# Filter
df[df["Score"] > 90]
df.query("Score >= 85")

# Group & aggregate
df.groupby("Name")["Score"].mean()

# Merge
pd.merge(left, right, on="key", how="left")

# Time series
df["Date"] = pd.to_datetime(df["Date"])
df.set_index("Date").resample("W")["Score"].mean()
```

## 📝 Notes

- Each notebook ends with a **Mini Practice** section to reinforce the concepts.
- In Class 8, newer pandas versions deprecate the `"M"` and `"Y"` resample aliases; use `"ME"` and `"YE"` instead.
- Class 6 includes some Hinglish comments for easier understanding.

## 🛣️ Possible Next Steps

- Rolling and expanding window calculations
- Date-based filtering and slicing
- Reading/writing CSV and Excel files
- Visualization with Matplotlib / Seaborn
- A small end-to-end data analysis project

## 🤝 Contributing

Suggestions and improvements are welcome. Feel free to open an issue or submit a pull request.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
