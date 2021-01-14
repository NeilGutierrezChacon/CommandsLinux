# CommandsLinux


## Commandos basicos

- ls [ruta a listar] -> Lista los archivos.

- ls -a -> Lista los archivos ocultos.

- pwd -> Identifica el directorio actual.

- cd [ruta donde se movera] -> Cambia de directorio.

- mkdir [nombre del nuevo directorio] -> Crea un nuevo directorio.

- cp [archivo a copiar][ruta donde se copia] -> Copia un archivo.

- rm [archivo] -> Borra un archivo.

- mv [ruta del archivo][ruta donde se movara] -> Mueve un archivo.

- rmdir [directorio a eliminar] -> Borra un directorio (Tiene que estar basio).

> Todos los directorios contiene los archivos . y .., estos son punteros a directorios.


### ls [ruta]

Lista los elementos de la ruta indicada, por defecto lista el directorio actual.

- ls -a -> Muesta los archivos ocultos.

- ls -t -> Ordena los archivos por fecha de modificación.

- ls -x -> Ordena los elementos primero por nombre y después por extensión.

- ls -X -> Ordena los elementos primero por extensión y después por nombre.

- ls -l -> Muestra toda la información (usuario, grupo, permisos, tamaño, fecha y hora de creación) de los elementos.

- ls -lh -> Muestra lo mismos que "ls -l" con unidades de tamaño en KB,MB.

- ls -R -> Muestra los elementos de los subdirectorios de forma recursiva.

- ls -S -> Ordena los resultados por tamaño de archivo.

## Editores de texto

Los mas importantes son

- vim [archivo] -> Hay que instalarlo.
- nano [archivo] -> Editor de texto installado por defecto en sistemas linux.

## Utilidades batch

Programas que procesan texto y emiten el resultado.

- cat [archivo] -> Muestra el contenido completo de un archivo.

- head [archivo] -> Nos muestra las primeras lineas de un archivo.

- head -n [numero de lineas] [archivo] -> Tambien podemos escoger cuantas lineas queremos visualizar.




## Como programar comandos

Para programar comandos podremos utilizar dos tipos de comandos.

- at

- crontab

### at [when] [time] [format_time]

* at now +2 minutes

Nos permite programar una serie de comandos que se ejecutaran una sola vez.

Para escapar una vez definidos los comandos hay que precionar ctrl+d.

### crontab [option]

* crontab -e

- -e Nos permite editar con el editor actualmente configurado la actual crontab.
- "*" Significa cualquier valor.

Nos permite generar una serie de comandos que se ejecutar de manera indefinida acorde a lo establecido en la tabla de configuración.

Nos habria un archivo con una explicasión basica de como usarlo y al final de este podremos programar nuestro comando con un formato de tabla.

Como el siguiente:

| m(Minutos) | h(Hora) | dom(DiaMes) | mon(Mes) | dow(DiaSemana) | Comando                     |
|------------|---------|-------------|----------|----------------|-----------------------------|
| 12         | 45      | *           | *        | *              | echo "Hola mundo">hola.txt" |