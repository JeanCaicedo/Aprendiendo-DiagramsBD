# Aprendiendo-DiagramsBD

![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![draw.io](https://img.shields.io/badge/draw.io-F08705?style=for-the-badge&logo=diagrams.net&logoColor=white)

Primeros pasos diseñando **diagramas entidad-relación** con draw.io (diagrams.net) y aprendiendo los fundamentos de la **normalización** de bases de datos relacionales.

Es un repositorio de **apuntes de aprendizaje**: teoría + tres diagramas de práctica (GA, zoo y uno sin título).

## Contenido

```
Aprendiendo-DiagramsBD/
├── GA.drawio                     # Diagrama ER de práctica (GA)
├── zoo.drawio                    # Diagrama ER de práctica (zoo)
├── Diagrama sin título.drawio    # Diagrama adicional
└── README.md                     # Apuntes de normalización
```

## Cómo abrir los diagramas

Los archivos `.drawio` se pueden abrir en:

- [draw.io desktop](https://www.drawio.com/)
- [app.diagrams.net](https://app.diagrams.net/) directamente en el navegador

---

## Apuntes de normalización

### Primera forma normal (1FN)

- Eliminar los grupos repetidos de las tablas individuales.
- Crear una tabla independiente para cada conjunto de datos relacionados.
- Identificar cada conjunto con una **clave principal**.
- No usar varios campos en una sola tabla para almacenar datos similares.

### Segunda forma normal (2FN)

- Crear tablas independientes para conjuntos de valores que se apliquen a varios registros.
- Relacionar estas tablas mediante **claves externas** (foreign keys).
- Los registros no deben depender de nada que no sea la clave principal.

### Tercera forma normal (3FN)

- Eliminar los campos que no dependan de la clave.
- Los valores que no son parte de la clave no pertenecen a esa tabla.
- Si un grupo de campos puede aplicarse a varios registros, conviene separarlos en su propia tabla.

> En la práctica, aplicar 3FN de forma estricta no siempre es conveniente: muchas tablas pequeñas pueden degradar el rendimiento. Suele aplicarse con criterio, priorizando los datos que cambian con frecuencia.

---

## Notas

- Los archivos `.$GA.drawio.bkp` y `.$zoo.drawio.bkp` que pueda haber en el repo son **backups temporales de draw.io** y no deberían estar versionados: lo correcto es agregarlos al `.gitignore` (`*.bkp`, `.$*`).
- Todo el contenido es material de estudio personal.

## Autor

Jean Caicedo — [@JeanCaicedo](https://github.com/JeanCaicedo)
