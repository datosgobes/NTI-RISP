!!! tip "Ejemplos prácticos de implementación"

    Aquí encontrarás prototipos listos para usar que demuestran cómo implementar el [modelo de metadatos NTI-RISP](/#modelo_de_metadatos) en diferentes formatos: [`RDF/XML`](https://www.w3.org/TR/rdf-syntax-grammar/) y [Turtle `(TTL)`](https://www.w3.org/TR/turtle/). 
    
    Estos ejemplos te guiarán en el uso de [propiedades obligatorias, recomendadas y opcionales](/#relacion_de_metadatos_del_modelo_nti-risp) para describir las entidades principales del modelo.

!!! example "Convenciones para la especificación de ejemplos"

    Se establece las siguientes convenciones de nombrado para su uso en todos los ejemplos definidos: 

    * Base de la URIs: `http://datos.gob.es`
    * URI catálogo: `http://datos.gob.es/catalogo` 
    * URI dataset: `http://datos.gob.es/dataset/dataset-ejemplo-1` 
    * URI distribución: `http://datos.gob.es/resource/distribucion-ejemplo-1` 
    * URI organismo: `http://datos.gob.es/recurso/sector-publico/org/Organismo/Identificador-Organismo`


# Catálogo - Clase: [`dcat:Catalog`](/#catalogo_-_clase_dcatcatalog_-_obligatorio)
## Catálogo - Propiedades
Este ejemplo ilustra la creación de un catálogo de datos conforme al perfil NTI-RISP, mostrando tanto las propiedades esenciales como las complementarias.

### Propiedades principales
El catálogo `http://datos.gob.es/catalogo` presenta toda la información fundamental:

* **Datos básicos**: Título claro y descripción detallada que lo identifica como el `Catálogo de Información Pública de la AGE`
* **Cronología**: Publicado el `27/11/2011` y actualizado el `10/01/2013`
* **Organización**: Enlazado a la entidad con código `E00004401`
* **Estructura**: Organizado mediante una taxonomía basada en sectores públicos
* **Acceso**: Disponible directamente a través de [datos.gob.es](http://datos.gob.es/datos/)

### Propiedades adicionales
Para mayor riqueza informativa, el catálogo también incluye:

* **Tamaño**: Contiene 850 documentos o recursos de información
* **Licencia**: Enlaza al [aviso legal](http://datos.gob.es/datos/?q=aviso-legal) correspondiente
* **Ámbito**: Cobertura geográfica: [España](http://datos.gob.es/recurso/sector-publico/territorio/Pais/España)
* **Contenido**: Referencia al conjunto de datos `http://datos.gob.es/catalogo/2332`

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/NTI-RISP_Catalog.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/NTI-RISP_Catalog.ttl"
    ```

# Conjunto de datos - Clase: [`dcat:Dataset`](/#distribucion_-_clase_dcatdistribution_-_obligatorio)
## Conjunto de datos - Propiedades
Este ejemplo muestra un conjunto de datos completo según la norma NTI-RISP, describiendo información catastral disponible en España.

### Propiedades principales
El dataset "Información catastral gráfica" ofrece cartografía catastral en formato vectorial:

* **Identificación básica**: Título claro y descripción detallada sobre la cartografía catastral vectorial gratuita
* **Categorización**: Pertenece al sector [vivienda](http://datos.gob.es/kos/sector-publico/sector/vivienda) y está etiquetado con palabras clave como `catastro`, `mapas`, `cartografía` e `inmuebles`
* **Publicación**: Generado por la organización E00004401, publicado el 26/12/2012
* **Actualización**: Frecuencia trimestral de actualización 
* **Multilingüe**: Disponible en español, gallego, inglés y catalán

###  Propiedades adicionales
El conjunto de datos incluye información complementaria relevante:

* **Cobertura**: Ámbito geográfico limitado a [España](http://datos.gob.es/recurso/sector-publico/territorio/Pais/España)
* **Validez temporal**: Período específico desde 26/12/2012 hasta 26/03/2013
* **Conformidad**: Cumple con estándares catastrales específicos (enlaces a resoluciones)
* **Acceso**: Proporciona enlaces a la Sede Electrónica del Catastro
* **Formatos**: Disponible en dos distribuciones diferentes (`SHP` y `ZIP`)

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/NTI-RISP_Dataset.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/NTI-RISP_Dataset.ttl"
    ```

# Distribución - Clase: [`dcat:Distribution`](/#distribucion_-_clase_dcatdistribution_-_obligatorio)
## Distribución - Propiedades
Este ejemplo muestra la forma correcta de documentar una distribución del conjunto de datos según la norma NTI-RISP.

Esta distribución es una de las formas en que se puede acceder a los datos catastrales descritos en el conjunto de datos principal, optimizada para usuarios que necesitan trabajar con información geoespacial en sistemas GIS.

### Propiedades de la Distribución
La distribución `http://datos.gob.es/catalogo/2332/SHP` proporciona el acceso a los datos catastrales en formato `ESRI Shapefile`:

* **Identificador único**: Referencia unívoca mediante [URI](http://datos.gob.es/catalogo/2332/SHP)
* **Título**: `Distribución en formato ESRI Shapefile` - indica claramente el formato de la distribución
* **Formato técnico**: Tipo MIME `application/octet-stream` correspondiente a archivos `SHP`
* **Documentación adicional**: Enlace a la página de ayuda para la descarga en formato Shapefile
* **Acceso directo**: URL completa para acceder directamente a la descarga
* **Tamaño**: Aproximadamente 30 MB (31.457.280 bytes)

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/NTI-RISP_Distribution.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/NTI-RISP_Distribution.ttl"
    ```

# Ejemplo de migración: Catálogo NTI-RISP a DCAT-AP-ES
Este ejemplo muestra cómo un catálogo modelado originalmente según NTI-RISP (2013) puede adaptarse al perfil [DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES). Sirve como plantilla para la transición porque mantiene la estructura básica del catálogo NTI-RISP y la enriquece con metadatos interoperables a nivel europeo, facilitando la integración en portales nacionales y europeos.

El catálogo `http://dcat-ap-es.ejemplo.org/catalogo` incluye información esencial como título, descripción, publicador, fechas clave, página web, temáticas, idiomas, términos de uso y referencia a datasets. Además, incorpora elementos recomendados por DCAT-AP-ES, como la cobertura geográfica y la alineación con vocabularios europeos, lo que permite una migración progresiva y compatible.

Este ejemplo es útil como plantilla porque:
- Muestra cómo mapear propiedades NTI-RISP a DCAT-AP-ES sin perder información relevante.
- Permite enriquecer el catálogo con nuevos metadatos exigidos por DCAT-AP-ES.
- Facilita la interoperabilidad y el cumplimiento de estándares europeos.
- Es fácilmente adaptable a otros catálogos NTI-RISP existentes.

!!! tip "Ejemplos disponibles"

    Puedes consultar versiones de ejemplo migradas al perfil DCAT-AP-ES en los siguientes enlaces:

    - [Catálogo NTI-RISP a DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES/examples/#catalogo_-_nti_dcatapes)
    - [Catálogo NTI-RISP a DCAT-AP-ES HVD](https://datosgobes.github.io/DCAT-AP-ES/examples/#catalogo_-_nti_dcatapes_hvd)

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/E_NTI-RISP_Catalog.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/E_NTI-RISP_Catalog.ttl"
    ```


# Plantilla de descripción de metadatos: Anexo VI. NTI-RISP (2013)
A continuación se muestra un modelo de representación para la descripción en RDF catálogo de datos, conjuntos de recursos de información y distribuciones asociadas. Representan las plantillas presentes en el [anexo VI de la NTI-RISP](https://www.boe.es/diario_boe/txt.php?id=BOE-A-2013-2380), con ejemplos de código expresado en RDF/XML y Turtle (TTL). En ambas plantillas se identifican variables, así como comentarios sobre los posibles valores a utilizar. 

En caso de que exista algún metadato que no tenga aplicación o no se conozca el valor, se representarán las propiedades. En ningún caso se indicarán elementos sin valor. 

!!! tip "Guías del catálogo nacional"

    Puedes encontrar las guías y plantillas originales en el portal de datos abiertos: [Guías de datos.gob.es](https://datos.gob.es/es/documentacion/guias-de-datosgobes)



## Plantilla RDF/XML para la federación de conjuntos de datos

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/NTI-RISP_Plantilla-AnnexoVI.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/NTI-RISP_Plantilla-AnnexoVI.ttl"
    ```

## Plantilla RDF/XML para la federación paginada

=== "RDF/XML"
    ```xml linenums="1"
    --8<-- "examples/rdf/NTI-RISP_Plantilla-AnnexoVI_pag.rdf"
    ```

=== "TTL"
    ```turtle linenums="1"
    --8<-- "examples/ttl/NTI-RISP_Plantilla-AnnexoVI_pag.ttl"
    ```