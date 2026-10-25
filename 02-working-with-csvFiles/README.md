# CSV Files with Pandas

Notes from my learning on reading CSV data with `pandas.read_csv()`.

`csv-files.ipynb` demonstrates the key parameters with small examples:

- Files: 'sep' (CSV/TSV), 'header', 'encoding'
- Selecting data: 'index_col' , 'usecols', 'skiprows', 'nrows'
- Cleaning while loading: 'dtype', 'parse_dates', 'converters', 'na_values'
- Large files:'chunksize'

## Run it

```bash
pip install pandas jupyter
jupyter notebook csv-files.ipynb
```
