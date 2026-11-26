<div align="center">
<table style="width:100; border:none;">
    <tr>
    <td align="left" style="border:none; width:20%;">
      <img src="imagenes/logotec.ong.png" width="160" alt="TecNM">
    </td>
    <td align="center" style="border:none; width:60%;">
    </td>
    <td align="right" style="border:none; width:20%;">
      <img src="imagenes/logoit.png" width="90" alt="ITMA II">
    </td>
  </tr>
</table>


# TECNOLOGICO NACIONAL DE MEXICO

## INSTITUTO TECNOLOGICO DE MILPA ALTA ll
<br>

### INGENIERÍA EN SISTEMAS COMPUTACIONALES

<br>
<br>

### ADMINISTRACION DE BASE DE DATOS
### DOCENTE. BOLLAS PAREDES DIEGO ALBERTO
<br>


### ANEXO
<br>

### 5° SEMESTRE
<br>

### JOSE GONZALEZ GUADALUPE NO. C. 241190024 
<br>

### 25 de noviembre de 2026
 </div>
<br>
<div style="page-break-after: always;"></div>

---

**ANEXO**

**Términos y herramientas  desconocidas de la práctica**

`Recuperación a un punto en el tiempo (PITR)`
Es un método de recuperación de bases de datos que combina un respaldo base (como un volcado SQL) con los registros de cambios posteriores (como el *binlog*) para llevar la base de datos a un estado exacto justo antes de que ocurra un error, pérdida o borrado accidental.

`Registro binario (`binlog`) y `mariadb-binlog` `
El registro binario (*binlog*) es un archivo donde MariaDB registra los eventos y cambios realizados en los datos (como inserciones, actualizaciones o eliminaciones) para auditoría, replicación o recuperación. La utilidad `mariadb-binlog` permite leer, filtrar y convertir esos eventos binarios en sentencias SQL legibles usando parámetros como `--start-position` y `--stop-datetime`.

 `--master-data=2`
Es una opción usada al generar respaldos lógicos que guarda en el archivo de respaldo (como comentario) el archivo *binlog* y la posición exacta en la que se encontraba el servidor al momento del respaldo, facilitando ubicar el punto de partida para la recuperación posterior.

`datadir` y ruta `/var/lib/mariadb/`
El `datadir` es el directorio donde MariaDB almacena sus bases de datos, tablas y archivos internos (incluidos los archivos *binlog* cuando se configuran sin otra ruta). En este entorno se verificó mediante `SHOW VARIABLES LIKE 'datadir';` que corresponde a `/var/lib/mariadb/`, por lo que usar esa ruta evitó errores de archivo no encontrado.

Tubería (`|`) y redirección (`>`) en Linux
En la terminal de Linux, la tubería (`|`) envía la salida de un comando directamente como entrada a otro (por ejemplo, pasar lo que genera `mariadb-binlog` hacia `mariadb -u root -p`), mientras que `>` redirige la salida hacia un archivo. La diagonal invertida (`\`) al final de una línea permite continuar escribiendo un comando largo en la siguiente línea para leerlo mejor.

`sudo` y `nano`
`sudo` permite ejecutar comandos con privilegios de superusuario/administrador en Linux, pidiendo la contraseña del usuario del sistema. `nano` es un editor de texto de terminal sencillo usado para revisar o modificar archivos de configuración como los de MariaDB.