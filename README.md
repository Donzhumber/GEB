# Identifying Rational Types in Unknown Environments under an Indirect Dynamic Mechanism

This repository contains the complete research project, replication codes, mathematical proofs, and microeconometric data calibration scripts associated with the paper **"Identifying Rational Types in Unknown Environments under an Indirect Dynamic Mechanism"**. Furthermore, all replication codes, data files, and supplementary materials are hosted in the public GitHub repository: \url{https://github.com/Donzhumber/GEB.git}, which includes a comprehensive README file detailing the contents of each directory.

The interactive dynamic simulation engine dashboard is deployed and accessible online:
*   **Live Streamlit Simulation Portal:** [https://y5ss6jtuccvpbdvuy7kdgl.streamlit.app/](https://y5ss6jtuccvpbdvuy7kdgl.streamlit.app/)

---

## Repository Structure

The directory is organized into five specialized folders, each serving a specific component of the research:

### 📂 [`main/`](./main/)
This directory contains the main research manuscript files and assets:
*   `Bernal_H_GEB.tex`: The main LaTeX source file formatted for *Games and Economic Behavior*.
*   `references.bib` & `econsoc.bst`: The BibTeX database and styling files.
*   `Figures/`: Folder housing the complete set of vector graphics (`.pdf` and `.png`) compiled in the main text.

### 📂 [`appendix_A/`](./appendix_A/)
This directory contains the empirical microeconometric calibration of the model:
*   `Appendix_A_Micro.tex` & `references_A.bib`: LaTeX documentation explaining the Stata data cleaning, VEC estimation, and competing risks Cox/Multinomial regressions.
*   `tables_cox_full.tex` & `tables_mnl_full.tex`: Core regression outputs loaded directly by the LaTeX document.
*   `scripts/`: Contains the `.do` replication scripts used in Stata to process the Centro Nacional de Memoria Histórica (CNMH) microdata and run estimations.

### 📂 [`appendix_B/`](./appendix_B/)
This directory contains the formal mathematical proofs and theorem verification:
*   `Appendix_B_Proofs.tex` & `references_B.bib`: LaTeX document detailing the mathematical proofs for the Rational Type Identification Theorem and the PBE Implementability Theorem.
*   `econsoc_B.bst`: Customized bibliographical style file.
*   `lean/`: Contains the complete **Lean 4 Interactive Theorem Prover** project where the logical dependency graph, algebraic transitions, and asymptotic limits of the convergence proofs have been formalized and verified.

### 📂 [`appendix_C/`](./appendix_C/)
This directory contains the interactive python-based simulation engine dashboard and deep learning value networks:
*   `app_DL.py`: The main Streamlit front-end application coordinates parameters and runs the period-by-period dynamic loop.
*   `train_captor_value_net.py` & `train_captor_true_type_net.py`: PyTorch-based neural network model files (`CaptorValueNet` MLP architecture) and training procedures.
*   `captor_value_net_T10.pt` & `captor_true_type_value_net_T10.pt`: Pre-trained neural network value approximation weight files.
*   `run_period.py`, `rational_behavior.py`, `model_logic.py`: Game logic, competing risks hazard drawers, and Bayesian posterior belief updates.
*   `run_app.command` (macOS) & `run_app.bat` (Windows): Double-clickable launcher shortcuts to run the app locally in Google Chrome with zero setup.
*   `README.md`: Setup and local installation instructions for the app.

### 📂 [`additional_documents/`](./additional_documents/)
This directory contains the administrative documents prepared for the Editorial Manager submission to *Games and Economic Behavior*:
*   `cover_letter.tex` / `cover_letter.pdf`: The official submission letter addressed to the Editors.
*   `highlights.tex` / `highlights.pdf`: Key novel contributions under the Elsevier 85-character limit.
*   `declaration_of_interest.tex` / `declaration_of_interest.pdf`: Ethics declaration regarding competing interests.
*   *(Spanish translations are also included for reference as `*_ES.tex` / `*_ES.pdf`).*

---

## Quick Launch: Running the Simulator Locally

If you wish to run the Streamlit portal locally rather than online:
1. Navigate to the **[`appendix_C/`](./appendix_C/)** folder.
2. Double-click **`run_app.command`** (if you are on macOS) or **`run_app.bat`** (if you are on Windows).
3. The script will automatically start the server and redirect Google Chrome to `http://localhost:8501`.
4. Detailed package requirements and step-by-step terminal execution instructions can be found in the folder's local **[README.md](./appendix_C/README.md)**.
