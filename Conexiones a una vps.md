<br><br>
#### Conexion remota por ssh (puerto 22)
>Conexion remota a una vps, para ejecutar comandos por consola
```bash
ssh root@192.168.0.1
```
- para estas conexiones se requieren un user, ip, y password

#### Transferecia de archivos por scp (puerto 22)
>Enviar cualquier tipo de archivo de tu maquina local a la vps
```bash
scp main.py root@192.168.0.1:/home/
```
- se indica primero el archivo que se quiere mandar (hay que estar en la misma carpeta en este caso)
- luego el user de la vps con su ip
- y por ultimo en que ruta de la vps queremos guardar este archivo (en este caso /home)

>Enviar muchos archivos de tu maquina local a la vps
```bash
scp main.py data.csv notas.txt root@192.168.0.1:/home/
```
- para mandar muchos archivos (que se encuentran en tu ubicacion actual) de una vez simplemente enlistarlos al principio

>Enviar todos los archivos de la carpeta actual a la vps
- imaginemos que estamos en la carpeta scraper y queremos enviar todos estos archivos (1 carpeta, 3 archivos) a una vps
```log
logs main.py data.csv requirements.txt
```
- la mejor forma de hacerlo es indicarle un punto en vez de enlistar todos los archivos
- el punto representa a todos los archivos de la carpeta actual
```bash
scp . root@192.168.0.1:/home/
```
