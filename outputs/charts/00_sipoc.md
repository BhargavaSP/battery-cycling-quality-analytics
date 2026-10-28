# SIPOC — Battery Cycling Quality Analytics

| Suppliers | Inputs | Process | Outputs | Customers |
|---|---|---|---|---|
| NASA Prognostics Center of Excellence | Raw .mat files (B0005, B0006, B0007, B0018) | 1. Parse NASA .mat files into tabular format | Long-format Parquet dataset | Quality Engineer (self) |
| MathWorks | MATLAB struct schema | 2. Validate measurements against NASA reference | MSA report (sub-1% agreement) | Capstone evaluators |
| Python open-source (NumPy, SciPy, pandas) | Numerical libraries | 3. Model capacity fade and predict RUL | Fade curves, decay fits, RUL predictions | Form Energy recruiters (portfolio audience) |
| Published literature (Form, Narayan group, ARPA-E) | Iron-air parameter ranges | 4. Build SPC charts, Cp/Cpk, Weibull model | Control charts, capability indices, reliability model | Future self (JMP replication phase) |
| JMP (SAS) | Statistical software | 5. Replicate pipeline in JMP for industry portability | JMP workflow, DMAIC report, Charter | GitHub public audience |