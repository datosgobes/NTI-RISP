Con el propósito de verificar si el intercambio de metadatos cumple técnicamente con el modelo de metadatos descrito por [NTI-RISP](/), se pueden utilizar los grafos de [formas SHACL disponibles en el repositorio](https://github.com/datosgobes/NTI-RISP/tree/main/shacl/). El Lenguaje de Restricción de Formas (*Shapes Constraint Language* - SHACL), es una [recomendación del W3C](https://www.w3.org/TR/shacl/]) para expresar restricciones en un grafo de conocimiento RDF. 

La siguiente ilustración muestra de forma esquemática las etapas principales del proceso de validación SHACL aplicadas a los metadatos, desde la preparación de los datos hasta la obtención de los resultados de conformidad.

![](img/dge_shacl.es.drawio "Ilustración . Descripción de los pasos de validación SHACL")

Las formas SHACL permiten comprobar si un catálogo expresado en una serialización RDF es válido. Dado que debería ser posible transformar el intercambio de datos en RDF para la conformidad con NTI-RISP, estas formas SHACL pueden utilizarse en cualquier contexto de intercambio de datos. Sin embargo las formas SHACL proporcionadas son solo un punto de partida para los implementadores.

Al utilizar estas plantillas es posible identificar y corregir posibles desviaciones respecto a la especificación, mejorando la calidad de los metadatos producidos. Además, existen herramientas interactivas, como el [Banco de Pruebas de Interoperabilidad de la Comisión Europea](https://www.itb.ec.europa.eu/shacl/any/upload) [^1] o [SHACL playground](https://shacl-playground.zazuko.com/) [^2], que ofrece un servicio en línea donde es posible cargar y validar archivos RDF contra las formas SHACL de NTI-RISP., que facilitan la validación de archivos DCAT-AP utilizando SHACL. ​

!!! info "Más información"

    - **✅ Cómo usar los validadores SHACL en diferentes stacks tecnológicos**: [github.com/datosgobes/NTI-RISP/.../shacl/README.md](https://github.com/datosgobes/NTI-RISP/tree/main/shacl/README.md)

    - Más información sobre la validación y las formas SHACL en [SHACL, un lenguaje para validar grafos RDF](https://datos.gob.es/es/blog/shacl-un-lenguaje-para-validar-grafos-rdf).

    
# Formas SHACL de NTI-RISP
Todas las versiones de los ficheros de formas de NTI-RISP se encuentran en el repositorio de código [`shacl/{version}/`](https://github.com/datosgobes/NTI-RISP/tree/main/shacl/): 

- `nti-risp_common_shapes.ttl`: Restricciones comunes para todas las entidades.
- `nti-risp_catalog_shape.ttl:` Restricciones para catálogos.
- `nti-risp_dataservice_shape.ttl`: Restricciones para servicios de datos.
- `nti-risp_dataset_shape.ttl`: Restricciones para conjuntos de datos.
- `nti-risp_distribution_shape.ttl`: Restricciones para distribuciones.
- `nti-risp_dataservice_shape.ttl`: Restricciones para servicios de datos.
- `nti-risp_mdr-vocabularies.shape.ttl`: Vocabularios controlados y sus restricciones.
- `nti-risp_imports.ttl`: Definiciones de importación para ontologías externas.
- `nti-risp_mdr_imports.ttl`: Definiciones de importación para vocabularios MDR.

**`hvd/`**: Subdirectorio con restricciones adicionales para conjuntos de datos de alto valor (HVD):

- `nti-risp_common_hvd_shapes.ttl`: Restricciones comunes para todas las entidades HVD.
- `nti-risp_catalog_shape.ttl:` Restricciones para catálogos HVD.
- `nti-risp_dataservice_hvd_shape.ttl`: Restricciones para servicios de datos HVD.
- `nti-risp_dataset_hvd_shape.ttl`: Restricciones para conjuntos de datos HVD.
- `nti-risp_distribution_hvd_shape.ttl`: Restricciones para distribuciones HVD.

# Casos de Uso
*Sección no normativa*

Los diferentes casos de validación para NTI-RISP se basan en el nivel de completitud de las comprobaciones y en la incorporación de conocimiento de fondo (vocabularios). Cada caso está diseñado para un escenario específico de intercambio de datos.

A continuación, se describen los casos con las formas para la versión `NTI-RISP 1.0.0` y se recomienda cuál utilizar para un catálogo:

## **Caso 1: NTI-RISP completo (con conocimiento de fondo)** {#case_1_nti_risp_full_imports}
Incluye todas las restricciones necesarias para la coherencia técnica de las distintas entidades del modelo, incluyendo las restricciones de pertenencia a clases de rango y todos los vocabularios utilizados en NTI-RISP con conocimiento de fondo, añadiendo conformidad con estándares externos.

*Formas SHACL*:

- *Estándar: Entidades principales y vocabularios controlados*
  - [`nti-risp_common_shapes.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_common_shapes.ttl)
  - [`nti-risp_catalog_shape.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_catalog_shape.ttl)
  - [`nti-risp_dataservice_shape.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_dataservice_shape.ttl)
  - [`nti-risp_dataset_shape.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_dataset_shape.ttl)
  - [`nti-risp_distribution_shape.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_distribution_shape.ttl)
  - [`nti-risp_mdr-vocabularies.shape.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_mdr-vocabularies.shape.ttl)

- *Importaciones*
  - [`nti-risp_imports.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_imports.ttl)
  - [`nti-risp_mdr_imports.ttl`](https://datosgobes.github.io/NTI-RISP/releases/1.0.0/shacl/nti-risp_mdr_imports.ttl)

!!! info "¿Qué es el conocimiento de fondo?"
    El conocimiento de fondo (*background knowledge*) consiste en la importación de ontologías y vocabularios externos que complementan la validación. Estos archivos de importación (`nti-risp_imports.ttl` y `nti-risp_mdr_imports.ttl`) contienen definiciones de clases, propiedades y relaciones jerárquicas de los estándares utilizados en NTI-RISP.
    
    Utilizar este conocimiento de fondo permite:
    
    1. *Validaciones semánticamente más ricas*: Al conocer la estructura completa de las ontologías.
    2. *Inferencia de tipos*: Permite detectar inconsistencias en la jerarquía de clases.
    3. *Validación de propiedades derivadas*: Comprueba relaciones que podrían no estar explícitas en los datos.
    
    Sin embargo, incluir este conocimiento de fondo puede hacer que la validación sea más lenta y consuma más recursos.

[^1]: SHACL validator: [github.com/ISAITB/shacl-validator](https://github.com/ISAITB/shacl-validator). Interoperability Test Bed, Interoperable Europe Unit, DIGIT, European Commission.
[^2]: Zazuko SHACL Playground: [github.com/zazuko/shacl-playground](https://github.com/zazuko/shacl-playground). Zazuko GmbH.