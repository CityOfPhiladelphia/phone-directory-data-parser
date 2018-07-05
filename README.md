# Phone directory data parser

Processes the files to support the [phone directory](http://www.phila.gov/phonedir).

## usage
Install [csvkit](http://csvkit.readthedocs.io/en/1.0.3/index.html) and run:

```bash
in2csv --format fixed --schema layout.csv --skip-lines 1 INPUT_FILE.txt
```

This command parses as text file to a CSV file, specifying that the document
uses a fixed-width format, providing a layout file for those widths, and
skipping the first line (which appears to be a malformed header).

You can then use a tool like [the-el](https://github.com/CityOfPhiladelphia/the-el)
to load the CSV file into a database, with the schema defined by `schema.json`.
