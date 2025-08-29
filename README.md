# PRISM2GSN: Eclipse Plug-in for Transforming PRISM Artefacts into GSN

## 📘 Overview
**PRISM2GSN** is an Eclpse plugin for transforming PRISM specifications and verification results into Goal Structuring Notation (GSN) assurance arguments. These arguments are created in the DSL of the AdvoCATE assurance case tool and are automatically regenerated when the artefacts change.

👉 Full **User Guide (with images)**: `https://github.com/DhamindaA/prism2gsn-eclipse-plugin/blob/main/prism2gsn-userguide.pdf`  
Release: https://github.com/DhamindaA/prism2gsn-eclipse-plugin/releases/tag/v1.0.0

> **Platform:** Windows 10/11 (x86_64) only. macOS/Linux are **not supported** in this release.

---

## 🛠 Prerequisites
- **Java 21 (JDK)** — check: `java -version`
- **Eclipse IDE for RCP and RAP Developers** 2025-03 (4.35.0) or newer
- **PRISM Model Checker (Windows)** e.g., **4.8.1** installed locally  
  (You will set the **PRISM bin directory**, e.g. `C:\Program Files\prism-4.8.1\bin` containing `prism.bat`.)

---

## ⬇️ Get the Project
- Download the ZIP from **Releases**:  
  https://github.com/DhamindaA/prism2gsn-eclipse-plugin/releases/tag/v1.0.0

---

## ▶️ Run in PDE (Runtime Workbench)
> This workflow does **not** install anything into Eclipse. It runs in a second Eclipse window (runtime workbench).

1. **Import (dev workspace)**  
   `File → Import → General → Existing Projects into Workspace` → **Select archive file** (the ZIP) → **Finish**.
2. **Launch runtime Eclipse**  
   Right-click project → `Run As → Eclipse Application` (opens the **runtime** window).
3. **Configure PRISM (runtime window)**  
   `Window → Preferences → PRISM Settings` → set **PRISM bin directory** (e.g., `C:\Program Files\prism-4.8.1\bin`) → **Apply & Close**.

---

## 🚀 Use the Plug-in (runtime window)
1. Create a project (e.g., `TestPrism`).
2. Add `model.prism` and `properties.props` **in the same folder** (one property per line).
3. Generate GSN:
   - **On Save:** edit & **Save** `properties.props` → creates `properties.props.arg.dsl`
   - **Context Menu:** right-click `properties.props` → **Generate GSN Fragment**

---

## 🧩 Troubleshooting
- **“PRISM not found” / `CreateProcess error=2`** → Set PRISM path **in the runtime window** under **PRISM Settings** (folder must contain `prism.bat`).
- **No `.arg.dsl` on save** → Ensure a `*.props` file is next to a `*.prism`/`*.pm` model; edit & save or use the context menu.
- **Context menu missing** → Right-click the **`.props`** file (not a folder).
- **Import/build errors** → Use **Eclipse RCP/RAP 2025-03+** and **JDK 21**.

---

## ⚠️ Limitations
- Windows-only artifact in this release.
- PRISM path is stored **per runtime workspace** (set it again if you launch a new runtime workspace).
- Multi-property generation expects **one property per line** in `*.props`, co-located with the model.

---

## 📄 User Guide, Releases, Contact
- **User Guide (PDF):** https://github.com/DhamindaA/prism2gsn-eclipse-plugin/blob/main/prism2gsn-userguide.pdf
- **Releases:** https://github.com/DhamindaA/prism2gsn-eclipse-plugin/releases/tag/v1.0.0
- **Contact:** Dhaminda.Abeywickrama@manchester.ac.uk

---

## 📜 License
The PRISM2GSN plug-in is provided **for academic and research use only**.  
Redistribution, modification, or commercial use is not permitted without prior written permission from the author.
