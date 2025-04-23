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
```
🧩 CUPFrameworkNET.dll (.NET / Unity)
📁 Folder: /CUP_NET

Implementations: CUPSimple, CUPPlusPlus, CUPFourPlus

Interface: IUniversalBrain

Uses math.tanh, atanh, and real matrix inversion

Save/load to .bin

Compatible with Unity, Blazor, WPF, etc.

🎮 Unity Integration
Place CUPFrameworkNET.dll in Assets/Plugins/

Use any class via:
```bash
using CUP;

IUniversalBrain brain = new CUPFourPlus();
float[] output = brain.Forward(input);
float[] reversed = brain.Inverse(output);
```
You can also use CUPSimple or CUPPlusPlus.

🧪 Training & Portability
✅ Train in Python (recommended)
```bash
from universal_cup import CUPBase
brain = CUPBase(size=4)

# ... training code (gradient, symbolic, evolution ...)
brain.save("trained_model.npz")
```
🔄 Export .npz to .bin (for Unity/.NET)
```bash
import numpy as np
data = np.load("trained_model.npz")
with open("brain_model.bin", "wb") as f:
    f.write(data["W1"].astype(np.float32).tobytes())
    f.write(data["W2"].astype(np.float32).tobytes())
    f.write(data["b1"].astype(np.float32).tobytes())
    f.write(data["b2"].astype(np.float32).tobytes())
    # Add W3, b3, mu/sigma if CUP++ / CUP++++
```

Then load in Unity or C#:
```bash
brain.Load("brain_model.bin");
```

🧠 CUP Levels

```bash
Level	Class / File	Features
CUP	CUPSimple	2 layers, tanh, invertible
CUP++	CUPPlusPlus	3 layers, stacked tanh, invertible
**CUP++++`	CUPFourPlus	Normalization + full analytic inversion
```

All models are:

Analytically defined

Fully invertible

Save/load compatible across Python and Unity

🔐 License
This framework is free for academic, scientific and student use.
Commercial use, resale, or redistribution is prohibited without explicit authorization.

For business licensing, please contact the author.

👤 Author
CUP-Framework created by a developer in symbolic and invertible artificial intelligence.
📧 contact@dfgamesstudio.com

🔁 Mise à jour README complet avec explication Python / .NET / Unity + entraînement
