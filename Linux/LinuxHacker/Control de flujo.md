
Se pueden concatenar dos o mas commandos con ayuda de el ";". Por ejemplo:
```bash
> whoami; ls -la
```

También se pueden concatenar con `&&` o `||`, al igual que en los lenguajes de programación, los commando se van a ejecutar con el `&&`, solo si el primer commando puede ejecutar o retorna un código de ejecución igual a 0, a diferencia de el `||` que se puede ejecutar el ultimo o el segundo independientemente si uno falla.

##### 'command' 2>/dev/null
Ese commando sirve en especial para que el output de el error no parezca en la terminal, el commando de ejecutara, pero en caso de retornar un código de ejecución diferente a 0, su std err (error) no se imprimirá en la terminal (eso lo indica ese 2).
Por otra parte el `/dev/null` es como un agujero negro. Todo lo que se mueva a ese directorio desaparecerá. 

##### 'command' &>/dev/null
No se vera ni el std err ni el std out

##### 'command' &>/dev/null &
Ese commando pasa a segundo plano algún programa que se este ejecutando colgado de la consola y no quieres ni que se vea el std out ni te moleste el echo de que no puedas ejecutar commandos. 
También se puede agregar un `disown` al final para poder cerrar la terminals sin que se cierre el programa que se esta utilizando.
