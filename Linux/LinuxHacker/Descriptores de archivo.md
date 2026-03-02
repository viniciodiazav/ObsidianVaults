
Este tema tiene relación con el Control de flujo [[Control de flujo]]

##### exec 3<> file
Creare un archivo identificado por el numero 3
>El `<>` quiere decir que el archivo tiene **capacidad de lectura y escritura**
>Si solo tuviese '<', la capacidad seria solo de lectura, y si quiero escribir es con un >

##### whoami >&3
Esa es una forma de enviar el output de el commando al descriptor de archivo
**Lo mete en formato append**

###### exec 3>&-
Ese commando hará que ya no sea posible escribir en el descriptor de archivo 

```bash
> exec 5<> data # descriptor de archivo con capacidad de lectura y escritura identificado con el 5
> whoami >&5 # el output de el commando escribelo en el identifiacdor de arcivo 5
> exec 8>&5 # lo que este en el identificador de archivo 5 quiero que sea una copia para el 8 y veceversa
> who >&8 # el output se vera reflejado como si se hubiera echo con el identifiacdor de archivo 5 (es como un puntero)
```

	