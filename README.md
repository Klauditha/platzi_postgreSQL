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


## Archivos de configuración

A través de la sentencia ```SHOW config_file``` se nos muestra donde están los archivos de configuración. En mi caso la ruta es: /Library/PostgreSQL/12/data/postgresql.conf

Algo a tener en cuenta es que en la ruta por default de instalación no se puede acceder debido a falta de permisos. Para ingresar basta con un:

sudo cd /Library/PostgreSQL/12/data/

Postgresql.conf: Configuración general de postgres, múltiples opciones referentes a direcciones de conexión de entrada, memoria, cantidad de hilos de pocesamiento, replica, etc.

pg_hba.conf: Muestra los roles así como los tipos de acceso a la base de datos.

pg_ident.conf: Permite realizar el mapeo de usuarios. Permite definir roles a usuarios del sistema operativo donde se ejecuta postgres.

## Tipos de Datos

### Principales

- Numéricos
- Moretarios
- Texto
- Binarios
- Fecha/Hora
- Boolean

### Especiales

- Geométricos: Con X y Y permiten calcular distancias y areas.
- Dirección de Red: Almacena IPs y permite hacer calculos de mascaras de red.
- Texto tipo bit: Calculos en hexadecimal y binario por ejemplo.
- XML, JSON
- Arreglos: Vectores y matrices.

- https://www.todopostgresql.com/postgresql-data-types-los-tipos-de-datos-mas-utilizados/
- https://www.postgresql.org/docs/11/datatype.html


## Utilidades

- Obtener fecha actual
    ```SELECT current_date```

## Particiones

- Separación fisica de datos
- Estructura lógica

    ```CREATE TABLE bitacora_viaje201001 PARTITION OF bitacora_viaje
        FOR VALUES FROM ('2010-01-01') TO ('2019-01-31')```

