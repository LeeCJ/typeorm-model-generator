# typeorm-model-generator

[Kononnable/typeorm-model-generator](https://github.com/Kononnable/typeorm-model-generator)

 为保证实体的正常使用，请更新typeorm到typeorm@0.2.0-alpha.44以上版本

```
npm i typeorm@next
```
## Usage

```shell
Usage: typeorm-model-generator -h <host> -d <database> -p [port] -u <user> -x
[password] -e [engine]

Options:
  --help                 Show help                                     [boolean]
  --version              Show version number                           [boolean]
  -h, --host             IP adress/Hostname for database server
                                                          [default: "127.0.0.1"]
  -d, --database         Database name(or path for sqlite)            [required]
  -u, --user             Username for database server
  -x, --pass             Password for database server              [default: ""]
  -p, --port             Port number for database server
  -e, --engine           Database engine
          [choices: "mssql", "postgres", "mysql", "mariadb", "oracle", "sqlite"]
                                                              [default: "mssql"]
  -o, --output           Where to place generated models
                            [default: "Z:\Repos\typeorm-model-generator\output"]
  -s, --schema           Schema name to create model from. Only for mssql and
                         postgres
  --ssl                                               [boolean] [default: false]
  --noConfig             Doesn't create tsconfig.json and ormconfig.json
                                                      [boolean] [default: false]
  --cf, --case-file      Convert file names to specified case
                 [choices: "pascal", "param", "camel", "none"] [default: "none"]
  --ce, --case-entity    Convert class names to specified case
                          [choices: "pascal", "camel", "none"] [default: "none"]
  --cp, --case-property  Convert property names to specified case
                          [choices: "pascal", "camel", "none"] [default: "none"]
  --lazy                 Generate lazy relations      [boolean] [default: false]
  --generateConstructor  Generate constructor allowing partial initialization
                                                      [boolean] [default: false]
```

### Examples

```
typeorm-generator -h 127.0.0.1 -p 3306 -d dbname -u root -x pwd -e mysql -o . --ce pascal --cp camel
```
