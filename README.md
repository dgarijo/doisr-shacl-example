## Very simple SHACL-based and JSON-schema based project

The goal of this sample repository is to provide a side by side comparison of JSON-schema and SHACL

### Setup
Create a new environment in Python 3.11 or bigger: `conda create -n pyshacl_3_11 python=3.11`

To activate the environment: `conda activate pyshacl_3_11`

Then install the requirements: `pip install -r requirements.txt`

This will install the dependencies for bot projects.

### JSON schema
With 
```
python -m jsonschema -i data/json/data_ok.json jsonschema/schema.json 
```

```
python -m jsonschema -i data/json/data_not_ok.json jsonschema/schema.json 
```



### SHACL

The following command: 
```
pyshacl -s shapes/shapes_example.ttl data/json_ld/data_ok.jsonld -df json-ld
```
will run a successful example in SHACL

The following command:
```
pyshacl -s shapes/shapes_example.ttl data/json_ld/data_not_ok.jsonld -df json-ld
```
will run an example where the shapes do not comply. Try to fix it


