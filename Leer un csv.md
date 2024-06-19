
#### Leer un csv usando la libreria csv
```python title:main.py
import csv

# Indica la ruta del archivo 
# como esta en la carpeta actual solo indica el nombre del archivo
archivo_csv = 'datos.csv'

# Abre el archivo CSV en modo lectura
with open(archivo_csv, 'r') as file:
    csv_reader = csv.reader(file) # Guarda el contenido del csv en la variable csv_reader

    for row in csv_reader: # Itera por cada fila del contenido y las va imprimiendo
        print(row)
```

> Por defecto el separador es una coma, para cambiarlo modificar esta linea:
```python title:main.py
csv_reader = csv.reader(file, delimiter=';')
```
- en este caso toma como delimitador el ;

> Para no imprimir la primer fila que es la que contiene el nombre de las columnas
```python title:main.py
import csv

archivo_csv = 'datos.csv'

with open(archivo_csv, 'r') as file:
    csv_reader = csv.reader(file) 

    next(csv_reader) # Saltar primer fila del csv

    for row in csv_reader:
        print(row)
```
- solo hace falta agregar next(csv_reader) que saltea la primer fila antes de iterar