# 🧠 CUP-Framework

**Universal Parametric Brain Architecture** — `CUP`, `CUP++`, `CUP++++`

> Modular, invertible, and analytically defined neural brains for symbolic and interpretable AI.

---

## 📦 What is CUP?

CUP is a family of compact neural modules, designed to be:
- Fully **analytically invertible**
- **Stackable** (CUP, CUP++, CUP++++)
- **Interpretable** and math-first
- **Protectable** via `.pyd` / `.dll` compilation

You can use it in **Python**, in **C#/.NET**, or **Unity**.

---

## 🐍 Python Version (`CUPBase` – Cython compiled)

🔧 Source: [`/CUP_Python`](./CUP_Python)

### Features:
- ✅ `forward()` and `inverse()` defined analytically
- ✅ Save/load as `.npz`
- ✅ Compiled via Cython (`.pyd`/`.so`)
- ✅ 100% real, invertible logic

```bash
pip install cython numpy
python setup.py build_ext --inplace
python test_cup.py

