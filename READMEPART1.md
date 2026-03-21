# Pagination & Metadata
## Parte 1 del laboratorio
#### Link del video de explicación: https://drive.google.com/file/d/1KDKP_wBTvCM5Y_QmisLrZ4cIvcn_isuf/view?usp=drive_link

En esta parte se modifico el backend para permitir que se puedan añadir parametros para filtrar las propiedades mostradas, tanto como filtrar el numero de pagina y el limite
de propiedades que pueden aparecer, mostrando los datos importantes de cada una de ellas y manejando correctamente los errores o cuando no hay datos para mostrar.

## Definition of Done

| Criterio            | Descripción                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| Parámetros de consulta | `?page=1&limit=10` funciona correctamente                                  |
| Metadatos en la respuesta | La respuesta incluye `{ data, meta: { total, page, limit, pages } }`     |
| Conteo total        | `meta.total` muestra la cantidad real de registros que coinciden            |
| Cálculo de páginas  | `meta.pages = ceil(total / limit)`                                           |
| Páginas vacías      | Retorna un arreglo `data` vacío, no un error                                |
| Valores por defecto | `page=1`, `limit=10` si no se especifican                                   |
| Validación          | Rechaza valores negativos o no numéricos                                     |

