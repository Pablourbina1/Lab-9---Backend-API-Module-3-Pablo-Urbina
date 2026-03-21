# Property Statistics
## Parte 2 del laboratorio
#### Link del video de explicación: https://drive.google.com/file/d/1UdTae_RBQya6bDmAnlIty8uUn6vd5Nl0/view?usp=drive_link

En esta parte se añadio un apartado al backend para visualizar unicamente las estadisticas de las propiedades, retornando sus datos más importantes y generales, como rango de
precios, total de propiedades, agrupar las propiedades dependiendo de su tipo (Terreno, Oficina, etc.), regresando todo correctamente.

## Definition of Done

| Criterio             | Descripción                                                       |
|----------------------|-------------------------------------------------------------------|
| Endpoint existente   | `GET /api/properties/stats` retorna datos        |
| Conteo por tipo      | `{ house: 10, apartment: 15, ... }`                              |
| Precio promedio      | Precio promedio por tipo de propiedad                            |
| Rango de precios     | `{ min: 50000, max: 2000000 }`                                   |
| Conteo total         | Número total de propiedades                                      |
| Agregación con Prisma| Utiliza `groupBy` y `aggregate`                                  |
| Base de datos vacía  | Retorna ceros, no errores                                        |


