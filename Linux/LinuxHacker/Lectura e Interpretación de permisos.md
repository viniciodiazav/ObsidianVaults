
En Linux tenemos una forma de describir el permiso de un archivo directorio, un ejemplo es el siguiente:
```bash
.rw-rw-r-- viniciod viniciod   0 B Sun Mar  1 23:34:21 2026 text.txt
```

Segmentado quedaría de la siguiente forma:
- Al principio aparecerá un . o una d. Un . quiere decir que es un archivo y una d que es un directorio
- el siguiente segmento seria .<u>rw-</u>rw-r-- el cual, r = readable, w = writable y en caso de haber un x quiere decir que tiene permisos de ejecución (rwx)
- Se dividen en tres segmentos de 3 caracteres, el primer segmento de 3 son los permisos de el propietario, la siguiente tercia son los permisos de los grupos y la ultima es el permiso de otros
- El propietario y el grupo se pueden ver con los nombres que aparecen después de la descripción de permisos. En este ejemplo `viniciod viniciod`
>El nombre de el propietario y el de el grupo no necesariamente tienen que ser el mismo

