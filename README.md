# NumPy Mastery — From Core Concepts to ML Applications

A structured, progressive collection of Jupyter notebooks covering NumPy from first principles through advanced algorithm implementations and real-world machine learning preprocessing tasks.

---

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Notebooks](#notebooks)
  - [01 — Core NumPy](#01--core-numpy)
  - [02 — NumPy Exercises (Beginner Set)](#02--numpy-exercises-beginner-set)
  - [03 — ML Applications](#03--ml-applications)
  - [04 — Advanced Algorithms](#04--advanced-algorithms)
  - [05 — Practice Drills](#05--practice-drills)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Topics Covered](#topics-covered)
- [Learning Path](#learning-path)

---

## Overview

This repository is a self-contained NumPy curriculum organized as a series of five notebooks. Each notebook builds on the previous one, progressing from basic array creation and indexing to implementing algorithms like 2D convolution, Kadane's 2D maximum subarray, histogram equalization, and ML-focused preprocessing pipelines — all using pure NumPy.

---

## Repository Structure

```
numpy-mastery/
│
├── 01_core_numpy.ipynb           # Foundation — all core NumPy concepts
├── 02_numpy_exercises.ipynb      # 21 beginner exercises (self-contained cells)
├── 03_ml_applications.ipynb      # 20 ML preprocessing tasks
├── 04_advanced_algorithms.ipynb  # 15 standalone algorithm implementations
├── 05_practice_drills.ipynb      # Structured drill set with bug-fixed solutions
│
└── README.md
```

---

## Notebooks

### 01 — Core NumPy

**File:** `01_core_numpy.ipynb`

The foundational reference notebook. Covers every major NumPy subsystem with clean, commented examples. Start here if you are new to NumPy or need a refresher.

| Section | What you'll learn |
|---|---|
| Array Creation | `np.array`, `arange`, `linspace`, `zeros`, `ones`, `eye`, `full`, `rand`, `randn`, `randint`, `empty` |
| Array Metadata | `.shape`, `.ndim`, `.size`, `.dtype`, `.itemsize` |
| Insert / Append / Delete | 1D, 2D, and 3D operations with `np.insert`, `np.append`, `np.delete` |
| Shape Manipulation | `reshape`, `flatten`, `ravel`, `T`, `astype` |
| Stacking & Splitting | `vstack`, `hstack`, `split`, `expand_dims`, `squeeze` |
| Indexing & Slicing | Basic, boolean, and fancy indexing |
| Aggregation | `sum`, `min`, `max`, `mean`, `std`, `var` with axis control |
| Math & Trig | `add`, `subtract`, `multiply`, `divide`, `power`, `sqrt`, `exp`, `log`, `sin` |
| Logical & Comparison | `==`, `where`, `any`, `all`, `logical_and` |
| Sorting & Searching | `sort`, `argsort`, `argmin`, `argmax`, `unique`, `searchsorted` |
| Copy vs View | Difference between `=`, `.copy()`, and views |
| Linear Algebra | `dot`, `matmul`, `inv`, `det`, `eig` |
| Random Module | `seed`, `choice`, `shuffle`, `permutation` |

---

### 02 — NumPy Exercises (Beginner Set)

**File:** `02_numpy_exercises.ipynb`

21 self-contained exercises. Each cell presents a problem and its clean solution. Ideal for practice after reading `01_core_numpy.ipynb`.

**Exercises include:**
- Building arrays with `arange`, `eye`, and `zeros`
- Boolean masking — replacing values greater than a threshold
- Reversing a 1D array with slicing
- Splitting arrays into equal parts
- Computing statistics: sum, mean, std, variance
- Dot products and element-wise multiplication via broadcasting
- Normalizing an array to the [0, 1] range
- Counting zeros, positives, and negatives
- Removing duplicate rows with `np.unique`
- Finding the row with the maximum sum
- Transposing with `swapaxes`

---

### 03 — ML Applications

**File:** `03_ml_applications.ipynb`

20 exercises applying NumPy to practical machine learning preprocessing scenarios. All implementations use pure NumPy — no pandas, scikit-learn, or other ML libraries.

**Key tasks:**
- **Missing value imputation** — fill `NaN` entries with per-column means using `np.nanmean`
- **Feature standardization** — Z-score normalization per column
- **Row normalization** — scale each row so its values sum to 1 (softmax-style)
- **One-hot encoding** — convert categorical labels to binary matrix without sklearn
- **Moving average** — time series smoothing with `np.convolve`
- **Manual matrix multiplication** — triple-loop implementation verified against `np.dot`
- **Image blurring** — mean filter applied with sliding 3×3 window
- **Weather simulation** — 365-day temperature array with 7-day rolling average
- **Recommendation matrix** — fill missing ratings with item-average imputation
- **Stock price analysis** — daily returns with `np.diff`, best buy day with `np.argmax`

---

### 04 — Advanced Algorithms

**File:** `04_advanced_algorithms.ipynb`

15 standalone, testable algorithm implementations. Each function is self-contained and includes a verification step or comparison against a NumPy built-in where applicable.

| # | Algorithm | Key technique |
|---|---|---|
| 1 | Spiral Matrix Generator | Boundary-walking fill |
| 2 | Sliding Window Maximum | Vectorized window slicing |
| 3 | Local Minima & Maxima Detection | Boolean array comparisons |
| 4 | Custom Padding | `np.full` + slice assignment |
| 5 | Trimmed Row Mean | `np.sort` + axis slicing |
| 6 | Histogram Equalization | CDF via `cumsum` + `np.interp` |
| 7 | Diagonal Sorting | `np.diagonal` + offset iteration |
| 8 | 2D Convolution (no scipy) | Manual sliding kernel application |
| 9 | Frequency Table | `np.unique` with `return_counts` |
| 10 | Random Block Shuffle | `reshape` + `swapaxes` + `shuffle` |
| 11 | Matrix Rank (no `linalg.matrix_rank`) | Manual Gaussian elimination |
| 12 | Maximum 2D Subarray Sum (Kadane's 2D) | Row compression + 1D Kadane |
| 13 | Array Diff Tracker | Element-wise change detection |
| 14 | Lexicographically Smallest Row | `np.lexsort` on transposed array |
| 15 | Mirror Matrix | `np.fliplr` and `np.flipud` |

---

### 05 — Practice Drills

**File:** `05_practice_drills.ipynb`

A structured, section-by-section drill set. Each section has a clearly stated problem followed by the correct solution. This notebook also serves as a corrected reference — it fixes several bugs present in earlier draft versions:

- **Fixed:** `arr[1:4]` → `arr[1:4, 1:4]` for correct 2D center extraction
- **Fixed:** `arr1[arr1 > 0]` → `arr1[arr1 < 0] = 0` for negative replacement
- **Added:** Missing diagonal zeroing exercise (`np.fill_diagonal`)
- **Removed:** Unused `import random`

| Section | Drills |
|---|---|
| 1 — Array Creation | Random integer array, `linspace` |
| 2 — Indexing & Slicing | Center 3×3 extraction, transpose |
| 3 — Shape Transformations | Reshape, flatten and restore |
| 4 — Masking & Filtering | Replace negatives, count above mean |
| 5 — Conditional Replacement | Negate even numbers |
| 6 — Row & Column Operations | Row normalization, diagonal zeroing |

---

## Prerequisites

- Python 3.8 or higher
- NumPy (`pip install numpy`)
- Jupyter Notebook or JupyterLab (`pip install notebook` or `pip install jupyterlab`)

No other dependencies are required. All notebooks use only the Python standard library and NumPy.

---

## Getting Started

**1. Clone the repository**
```bash
git clone https://github.com/<your-username>/numpy-mastery.git
cd numpy-mastery
```

**2. Install dependencies**
```bash
pip install numpy notebook
```

Or with conda:
```bash
conda install numpy notebook
```

**3. Launch Jupyter**
```bash
jupyter notebook
```

Then open notebooks in order, starting with `01_core_numpy.ipynb`.

---

## Topics Covered

| Topic | Notebooks |
|---|---|
| Array creation & metadata | 01, 02, 05 |
| Indexing, slicing, masking | 01, 02, 03, 05 |
| Shape manipulation | 01, 02, 03, 05 |
| Broadcasting | 01, 02, 03 |
| Aggregation & statistics | 01, 02, 03 |
| Linear algebra | 01, 03, 04 |
| Sorting & searching | 01, 02, 04 |
| Missing value handling | 03 |
| Normalization & standardization | 02, 03 |
| Convolution & filtering | 03, 04 |
| Algorithm implementation | 04 |
| Random module | 01, 03 |

---

## Learning Path

Follow the notebooks in numbered order for a structured progression:

```
01_core_numpy          ← Read and run every cell; build your mental model
       ↓
02_numpy_exercises     ← Attempt each problem before reading the solution
       ↓
03_ml_applications     ← Focus on understanding the ML context for each task
       ↓
04_advanced_algorithms ← Study each function; try rewriting from scratch
       ↓
05_practice_drills     ← Use as timed self-assessment or warm-up exercises
```

> **Tip:** After completing all five notebooks, revisit `04_advanced_algorithms` and try to vectorize any loops using NumPy broadcasting — a good way to deepen your intuition for how NumPy operations compose.
