# Excel con Dashboards

![logo](https://www.belatrix.com/wp-content/uploads/2023/08/belatrix-logosweb-1.png)

> Alan Badillo Salas (alan@belatrix.com)

```markdown
Módulo I – Fundamentos y modelado de datos con Excel

1.	Fórmulas de búsqueda y coincidencia
2.	Fórmulas de agregación
3.	Manejo de otras funciones clave
4.	Tablas estructuradas y concentrados
5.	Buenas prácticas en la preparación de datos
```

## E101 - Tabla de préstamo de libros

Una biblioteca tiene 10 libros y 10 usuarios.

Diseña una tabla en Excel para ayudar a administrar los préstamos.

> Columna `A` - Nombre de los usuarios

En la celda `A1` pon `Usuarios` seguido de 10 nombres diferentes para las celdas `A2`, `A3`, ..., `A11`, por ejemplo, `Alicia`, `Beto`, `Carla`, ...

> Columna `B` - Préstamo del *libro 1*

En la celda `B1` pon el nombre del libro, por ejemplo, `Principito` (usa nombres cortos). Seguido de 1 si el usuario tiene el libro o 0 sino.

**Nota:** Solo puede haber un 1 en toda la columna.

> Columnas `C`, `D`, ..., `K` - Préstamo del *libro j*

En las celdas `C1`, `D1`, ..., `K1` pon otros nombres de libros que tenga la biblioteca. Y rellena de 1 si el usuario tiene el libro o 0 sino.

## E102 - Verificar préstamos

Suma el total de usuarios que tienen prestado un libro, si es 0 o 1 es correcto, colorea de rojo en caso de que el valor sea mayor a 1.

> Utiliza `INDICE` y `COINCIDIR` para seleccionar todos los valores relacionados al libro (para todos los usuarios / vector columna), luego aplica `SUMA`

## E103 - Contar el número de libros por usuario

Para cada usuario, suma cuántos libros posee, si es 0 colorea en verde, si es 1 colorea en amarillo, si es 2 o más colorea en rojo.

> Utiliza `INDICE` y `COINCIDIR` para seleccionar todos los valores relacionados al usuario (para todos los libros / vector fila), luego aplica `SUMA`

## E104 - Tabla estructurada de préstamos

Crea una tabla estructurada sobre los libros, y en otra hoja proyecta los encabezados, los datos y los totales de suma.

### 105 - Reportes transversales

Genera un reporte vertical que indique el usuario que posee el libro como el siguiente:

```text
Libro 1     Alicia
Libro 2     -
Libro 3     Alicia
Libro 4     Daniel
Libro 5     -
Libro 6     Estefany
Libro 7     Daniel
Libro 8     -
Libro 9     Carla
Libro 10    Beto
```

* ¿Cómo podemos determinar el usuario qué tiene prestado un libro? Pista: `FILTRAR`
* ¿Cómo evitamos que se desborde el reporte si hay más de un usuario con el mismo libro? Pista: `INDICE`