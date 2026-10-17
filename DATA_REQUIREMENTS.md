# Source and input requirements

This staging set contains the original `ai.ipynb` with all saved outputs, execution counts, cell metadata, and attachments removed. **Every source cell is unchanged.** The small original `machine_l.csv` is included unchanged. This notebook has not been executed during source preparation.

The notebook contains three independent examples:

1. ERA5 temperature mapping requires an external `ERA5temp_1978_monthly.nc` file containing `t2m`, `latitude`, and `longitude`; the original notebook uses a machine-specific absolute path that the operator must configure before running. Dependencies: xarray, netCDF4, NumPy, Matplotlib, and Cartopy. Cartopy's geographic assets may require prior offline provisioning.
2. Convergent cross mapping reads the included `machine_l.csv`. Required columns: `Date`, `LWSC`, `Runoff`, `P`, `E`, `Area`, and `Runoff m3`. Dependencies: pandas and pyEDM. The original calls and parameters are preserved; compatibility with the selected pyEDM version has not been verified.
3. Flux-data regression visualization requires an external `GPPdyn.xlsx` workbook with `GPPdyn`, `GPP_DT`, and `type` columns. The original notebook again contains a machine-specific path. Dependencies: pandas, an Excel reader such as openpyxl, NumPy, Matplotlib, and seaborn.

The ERA5 and flux workbook data are not supplied here. Do not claim all cells are runnable without them. Original paths are retained in code to avoid silently changing the workflow; removed outputs no longer expose execution-time local paths or credentials.
