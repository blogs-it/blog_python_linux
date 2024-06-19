#### Creacion del proyecto
>Crear carpeta del proyecto y moverte a la carpeta
```bash
mkdir data_proyecto && cd data_proyecto
```
<br><br>
#### Verificaciones
> Verificar que el gestor de paquetes de python (pip) este instalado
```bash
pip3 --version  #Solo la primera vez en un sistema nuevo
```
> Verificar que el modulo virtualvenv este instalado
```bash
pip3 install virtualenv #Solo la primera vez en un sistema nuevo
```
<br><br>
#### Creacion del entorno
> Crear entorno virtual para poder instalar las librerias solamente en la carpeta del proyecto, 
> y que no se instalen a nivel global en la pc
```bash
python3 -m venv venv
```
-  -m: se usa para decirle al interprete de python que vamos a usar una libreria
-  venv: nombre de la libreria que queremos usar para crear el entorno
-  venv: (segundo venv) nombre de la carpeta donde se guardara la info del entorno

>Activar el entorno
```bash
source venv/bin/activate  #Comando solo cuando usas linux
```
-  source: comando de linux para ejecutar un archivo
-  venv/bin/activate: ruta en donde se encuentra el archivo activate, que es el cual 
activa el entorno
<br><br>
#### Ejemplo de instalar una libreria para usarla en un main.py
> Comando de instalacion
```bash
pip3 install pandas
```
-  pip3: se llama al gestor de paquetes de python
-  install: se le indica que queremos instalar una libreria
-  pandas: nombre de la libreria a instalar

> ***Opcion 1:*** Se crea un archivo (vacio) para despues editar y poder usar la libreria
```bash
touch main.py
```
> ***Opcion 2:*** Se abre un archivo nuevo con vim para crear el codigo y luego guardarlo
```bash
vim main.py
```
- Pasos para salir de vim:
1. Tocar escape para entrar en modo command
2. Tocar ( shift + : ) esto permite ingresar los comandos
3. Ingresar ( x ) en minuscula, para poder guardar y salir al mismo tiempo

> Codigo de ejemplo para usar pandas
```python title:main.py
import pandas as pd #Esto importa la libreria pandas con un alias pd

df_csv = pd.read_csv('data.csv') #Lee un csv llamado data.csv
print(df_csv)
```
> Ejecutar el codigo
```bash
python3 main.py
```
<br><br>
#### Para volver a ejecutar otro dia
1. Moverse a la carpeta del proyecto
```bash
cd data_proyecto
```
2. Iniciar el entorno
```bash
source venv/bin/activate
```
3. Ejecutar el archivo
```bash
python3 main.py
```

