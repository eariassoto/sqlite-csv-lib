# SQLite CSV Virtual table extension

This project compiles the SQLite extension to create virtual tables from CSV files. The code is available [here](https://sqlite.org/csv.html), in the sqlite official page.

## Usage: 

Compile the library:
```bash
sqlite-csv-lib$ mkdir build
sqlite-csv-lib$ cd build
sqlite-csv-lib/build$ cmake ..
sqlite-csv-lib/build$ make
```
Launch sqlite3:
```
sqlite> .load lib/libsqlite-csv-lib.so 
sqlite> CREATE VIRTUAL TABLE temp.csv USING csv(filename='sample-csv/cities.csv');
sqlite> SELECT * FROM csv;
```

