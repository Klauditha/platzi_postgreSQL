# Platzi Curso PostgreSQL

## Interacción Consola

- Para entrar a la consola
    ``` psql -U postgres -W ```

- Ver comandos
    ``` \? ```

- Listar todas las bases de datos
    ``` \l ```

- Ver las tablas de una BDD
    ``` \dt ```

- Cambiar a otra BDD
    ``` \c nombre_BD ```

- Describir una tabla 
    ``` \d nombre_tabla ```

- Ver todos los comandos SQL 
    ``` \h ```

- Ver como se ejecuta un comando SQL
     ``` \h nombre_de_la_funcion```

- Cancelar todo lo que hay en una pantalla
    ```  Ctrl + C ```

- Ver la version de Posgres instalada
    ``` SELECT version(); ```

- Volver a ejecutar la función realizada anteriormente
    ``` \g ```

- Inicializar el contador de tiempo para que la consola diga en cada ejecución cuanto demoro
    ``` \timing ```

- Limpiar pantalla de la consola PSQL
    ``` Ctrl + L ```