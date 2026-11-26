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


### CUESTIONARIO
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

## CUESTIONARIO

1. **¿Qué datos se habrían perdido si solo hubieras usado el respaldo de la Parte A?**

Se habrían perdido los 2 clientes nuevos después de hacer el respaldo quedando únicamente los 5 clientes iniciales en lugar de los 7.

2. **¿Para qué sirve la opción **`--master-data=2`**?**

Sirve para registrar dentro del archivo de respaldo el nombre del archivo binlog y la posición exacta en la que quedó el servidor al momento de tomar el respaldo. 

3. **¿Por qué es necesario activar el binlog antes de que ocurra el error?**

Porque el registro binario (binlog) guarda cada cambio que modifica los datos después de que el servidor está en marcha sii no está activado antes del error mariadb no graba las inserciones o cambios posteriores al respaldo y no hay forma de recuperar lo que paso entre el respaldo y el borrado.

4. **¿Por qué se esperaron 5 segundos antes y después de anotar la hora?**

Para separar con claridad en el tiempo las operaciones que sí queríamos conservar de la operación que queríamos evitar.
