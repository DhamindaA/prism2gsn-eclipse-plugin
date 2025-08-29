# PRISM2GSN (Eclipse Plug-in) — **Windows Only**

**PRISM2GSN** is an Eclipse plug-in that reads PRISM model-checking properties and generates GSN/AdvoCATE argument fragments. 


> **Platform support:** Windows 10/11 (x86_64) only.  
> macOS/Linux are **not supported** in this artifact.

---

## Quick Start (Windows)

### Prerequisites
- **Eclipse IDE for RCP and RAP Developers** 2025-03 (4.35) or newer
- **JDK 21** (e.g., Eclipse Adoptium or Oracle JDK)
- **PRISM Model Checker for Windows** (e.g., 4.8.1)

### Steps
1. **Import the project**  
   *File → Import → General → Existing Projects into Workspace* → select this project → **Finish**.
2. **Run the plug-in**  
   Right-click project → *Run As → Eclipse Application* (opens a **second Eclipse** window = runtime workbench).
3. **Configure PRISM path (in the runtime window)**  
   *Window → Preferences → PRISM Settings* → set **PRISM bin directory**, e.g.  
   `C:\Program Files\prism-4.8.1\bin` (must contain `prism.bat`) → **Apply and Close**.
4. **Test**  
   In the runtime window, create a project with:
   - `model.prism`
   - `properties.props` (properties **one per line**, in the same folder as the model)
5. **Generate GSN**
   - Edit & **Save** `properties.props` → creates `properties.props.arg.dsl`, **or**
   - Right-click `properties.props` → **Generate GSN Fragment**.

---

