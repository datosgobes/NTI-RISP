Esta sección recopila las preguntas más frecuentes sobre la NTI-RISP de 2013, su implementación y uso. El objetivo es proporcionar respuestas claras y concisas para facilitar la comprensión y adopción de este perfil de aplicación.

Secciones:

* [Perfiles de aplicación](#application-profile): Contextualiza las especificaciones relacionadas con el modelo de metadatos de la NTI-RISP.
* [Sobre NTI-RISP y DCAT-AP-ES](#nti-risp-dcat-ap-es): Aborda preguntas comunes sobre la inmplementación técnica de la NTI-RISP y su evolución: [DCAT-AP-ES](https://github.com/datosgobes/DCAT-AP-ES/).
* [Modelo de datos](#model): Explica dudas y conceptos fundamentales del modelo de datos.
* [Federación](#federation): Responde a dudas sobre la implementación técnica y la federación con el [catálogo nacional](https://datos.gob.es/).
* [Sobre el repositorio](#nti-risp-repo): Introduce el repositorio [`datosgobes/NTI-RISP`](https://github.com/datosgobes/NTI-RISP/) y su propósito.


!!! warning "Relación con las preguntas frecuentes de datos.gob.es"

    Este documento se centra en cuestiones específicas sobre el modelo de metadatos de la NTI-RISP y su implementación técnica. Para consultas generales sobre el catálogo nacional, recomendamos visitar las [preguntas frecuentes de datos.gob.es](https://datos.gob.es/faq-page).

---

## **Perfiles de aplicación** { .faq-h #application-profile}

<div class="grid cards" markdown>

-   :simple-semanticweb:{ .lg .middle .grid-emoji } **DCAT**{ .grid-title{ .grid-title #vocab-dcat }   

    ---  

    Es el vocabulario fundamental para describir catálogos y recursos de datos en la web desarrollado por el W3C.

    [:octicons-arrow-right-24: Ver más](https://www.w3.org/TR/vocab-dcat/)

-   :simple-europeanunion:{ .lg .middle .grid-emoji } **DCAT-AP**{ .grid-title #vocab-dcat-ap }  
 
    ---  

    Es el perfil europeo basado en DCAT que define normas comunes para catálogos de datos abiertos, facilitando la interoperabilidad. **El modelo de metadatos de la NTI-RISP de 2013 no es compatible**.

    [:octicons-arrow-right-24: Ver más](https://op.europa.eu/es/web/eu-vocabularies/dcat-ap)

-   :fontawesome-solid-star:{ .lg .middle .grid-emoji } **DCAT-AP HVD**{ .grid-title #vocab-dcat-ap-hvd} 

    ---  

    Extensión de DCAT-AP para describir y catalogar conjuntos de datos de alto valor en cumplimiento del Reglamento de Implementación HVD. **El modelo de metadatos de la NTI-RISP de 2013 no es compatible**.

    [:octicons-arrow-right-24: Ver más](https://interoperable-europe.ec.europa.eu/collection/semic-support-centre/solution/dcat-ap-hvd)

-   :boostrap-spain:{ .lg .middle .grid-emoji } **DCAT-AP-ES**{ .grid-title #vocab-dcat-ap-es } 

    ---  

    Adaptación de DCAT-AP que incorpora especificaciones propias del contexto español y la extensión HVD, y **evoluciona el modelo de metadatos de la NTI-RISP de 2013**.

    [:octicons-arrow-right-24: DCAT-AP-ES](https://github.com/datosgobes/DCAT-AP-ES)

</div>


---

## **Sobre NTI-RISP y DCAT-AP-ES** { .faq-h #nti-risp-dcat-ap-es}

<div class="grid cards" markdown>

-   :material-calendar:{ .lg .middle .grid-emoji } **¿Cuándo entro en vigor?**{ .grid-title #vigencia }

    ---

    La NTI-RISP entro en vigor el 5 de marzo de 2013, tras la aprobación y publicación en el BOE. DCAT-AP-ES se espera que entre en vigor a lo largo de 2025 tras la publicación en el BOE de la nueva NTI-RISP.
    
    [:octicons-arrow-right-24: NTI-RISP](https://www.boe.es/eli/es/res/2013/02/19/(4))

-   :material-clock-fast:{ .lg .middle .grid-emoji } **¿Qué plazo hay para migrar a DCAT-AP-ES?**{ .grid-title #migracion }

    ---

    Los publicadores disponen de un periodo de adaptación desde la entrada en vigor de la nueva Norma y el perfil de aplicación DCAT-AP-ES para migrar desde los modelos de metadatos dispuestos en la NTI-RISP de 2013.
    
    [:octicons-arrow-right-24: Cambios](https://datosgobes.github.io/DCAT-AP-ES/#annex-1-nti-risp-to-dcat-ap-es)

-   :material-connection:{ .lg .middle .grid-emoji } **¿Relación con otros estándares?**{ .grid-title #relacion }

    ---

    DCAT-AP-ES implementa DCAT-AP y su extensión HVD, garantizando la compatibilidad con el ecosistema europeo de datos abiertos.
    
    [:octicons-arrow-right-24: UML](/uml)

-   :fontawesome-solid-folder-open:{ .lg .middle .grid-emoji } **¿Hay materiales de apoyo?**{ .grid-title #materiales }

    ---

    Existe guía para la aplicación del modelo de datos, convenciones, vocabularios, ejemplos, guías y documentación, etc.
    
    [:octicons-arrow-right-24: Guía](/)

-   :fontawesome-solid-plus:{ .lg .middle .grid-emoji } **¿Principales diferencias con DCAT-AP-ES?**{ .grid-title #novedades }

    ---

    DCAT-AP-ES supone una evolución, se alinea con el perfil europeo DCAT-AP, incorpora servicios de datos (`dcat:DataService`), el modelado de conjuntos de alto valor (HVD) y mejoras en la descripción de la calidad de metadatos respecto del modelo de 2013.
    
    [:octicons-arrow-right-24: Clases](/#clases_del_perfil_de_aplicacion_dcat-ap-es)

-   :fontawesome-solid-building-columns:{ .lg .middle .grid-emoji } **¿Más información sobre la NTI-RISP?**{ .grid-title #novedades }

    ---

    Se puede obtener más información y apoyo documental de las Normas Técnicas de Interoperabilidad (NTI) publicadas en el BOE a través del Portal de la Administración electrónica (PAe).
    
    [:octicons-arrow-right-24: PAe](https://administracionelectronica.gob.es/pae_Home/pae_Biblioteca/pae_PublicacionesPropias/Monografias-administracion-electronica/Guias-de-aplicacion-NTI.html)

</div>

## **Modelo de datos** { .faq-h #model}

<div class="grid cards" markdown>

-   :fontawesome-solid-database:{ .lg .middle .grid-emoji } **¿Qué es un conjunto de datos (*dataset*)?**{ .grid-title #vocab-dcat }

    ---

    Un conjunto de datos (*dataset*, clase `dcat:Dataset`) es una colección de información relacionada sobre un tema, organizada para facilitar su acceso, uso y distribución por una organización.

    [:octicons-arrow-right-24: Conjunto de datos](/#dcat-dataset)

-   :fontawesome-solid-file:{ .lg .middle .grid-emoji } **¿Qué es una distribución?**{ .grid-title #vocab-dcat-ap }

    ---

    Una distribución (`dcat:Distribution`) es una representación específica de un conjunto de datos, como un archivo en un formato particular (ej: `CSV`, `JSON`).

    [:octicons-arrow-right-24: Distribución](/#dcat-distribution)

-   :fontawesome-solid-box-open:{ .lg .middle .grid-emoji } **¿Diferencias entre recurso y distribución?**{ .grid-title #vocab-dcat-ap-hvd}

    ---

    Un *recurso* (`dcat:Resource`) es una clase abstracta que representa elementos de un catálogo, como conjuntos, servicios u otros catálogos. Sirve de base para estos tipos, pero no se usa directamente. 
    
    En cambio, una distribución es una forma específica de acceder a ese recurso, como un archivo `CSV` descargable.

    [:octicons-arrow-right-24: Recurso (DCAT)](https://www.w3.org/TR/vocab-dcat/#dcat-scope)

-   :fontawesome-solid-book:{ .lg .middle .grid-emoji } **¿Qué es un registro de un catálogo?**{ .grid-title #vocab-dcat-ap-es }

    ---

    Un registro de catálogo (`dcat:CatalogRecord`) es un recurso que contiene los metadatos sobre entradas individuales de un dataset o servicio en un catálogo, no la descripción del recurso en sí. 
    
    Representa información administrativa como la fecha de incorporación al catálogo, estado de publicación o información de procedencia.

    [:octicons-arrow-right-24: Registro de Catálogo](/#dcat-catalogrecord)


</div>
<div class="grid cards grid-2col" markdown>

-   :fontawesome-solid-diagram-project:{ .lg .middle .grid-emoji } **¿Cómo se relacionan los elementos de NTI-RISP?**{ .grid-title #relaciones-modelo }

    ---

    El modelo de metadatos de la NTI-RISP funciona como una red donde los elementos se conectan entre sí:

    - Un **catálogo** (`dcat:Catalog`) funciona como un contenedor principal que aloja conjuntos de datos y servicios

    - Cada **conjunto de datos** (`dcat:Dataset`) puede tener múltiples distribuciones (formatos)

    - Las **distribuciones** (`dcat:Distribution`) pueden accederse a través de servicios específicos

    ```mermaid
    graph LR
        %% Definición de nodos
        Catalog((dcat:Catalog)):::main
        Dataset[dcat:Dataset]:::entity
        Distribution[dcat:Distribution]:::entity
        
        %% Relaciones con etiquetas
        Catalog -->|dcat:dataset| Dataset
        Dataset -->|dcat:distribution| Distribution
        
        %% Estilos con bordes redondeados
        classDef main fill:#B8C2CC,stroke:none,font-size:24px,color:#00a99d,font-weight:bold;
        classDef entity fill:#e6f3ff,stroke:none,font-size:20px,color:#154481 !important,rx:10,ry:10,font-weight:bold;
        
        %% Estilos de línea
        linkStyle default stroke:#154481,stroke-width:1px,stroke-dasharray:3;
    ```
    
    [:octicons-arrow-right-24: Relaciones](/#dcat-ap-es-model-relations)

</div>


---

## **Federación** { .faq-h #federation}

<div class="grid cards" markdown>

-   :fontawesome-solid-file-code:{ .lg .middle .grid-emoji } **¿Qué formato debe tener el catálogo?**{ .grid-title #implementacion-formatos }

    ---

    El fichero de catálogo que va a federarse debe describirse conforme a la sintaxis XML para RDF denominada `RDF/XML`

    [:octicons-arrow-right-24: Sintaxis](https://www.w3.org/TR/rdf-syntax-grammar/)

-   :fontawesome-solid-laptop-code:{ .lg .middle .grid-emoji } **¿Dónde encontrar ejemplos de NTI-RISP?**{ .grid-title #implementacion-ejemplos }

    ---

    Disponibles en la guía online y en el directorio `examples/` del repositorio, organizados por entidades y casos de uso específicos.

    [:octicons-arrow-right-24: Ejemplos](/examples)

</div>

---

## **Sobre el repositorio** { .faq-h #nti-risp-repo}

<div class="grid cards" markdown>

-   :material-source-repository:{ .lg .middle .grid-emoji } **¿Qué es el repositorio NTI-RISP?**{ .grid-title #general-repositorio }  

    ---

    Repositorio de código y seguimiento sobre la implementación de la Norma Técnica de Interoperabilidad de Reutilización de recursos de la información de 2013.

    [:octicons-arrow-right-24: Repositorio](https://github.com/datosgobes/NTI-RISP "Repositorio de código fuente con todo el material de NTI-RISP" )

-   :fontawesome-brands-readme:{ .lg .middle .grid-emoji } **¿Qué encontrar en el repositorio NTI-RISP?**{ .grid-title #general-readme }

    ---

    Una aproximación al modelo de metadatos de la NTI-RISP, su implementación y ejemplos.

    [:octicons-arrow-right-24: Léeme](https://github.com/datosgobes/NTI-RISP#guía-para-NTI-RISP "README del repositorio NTI-RISP con indicaciones sobre contenido y contribución" )

-   :fontawesome-solid-code-pull-request:{ .lg .middle .grid-emoji } **Pensado para contribuir**{ .grid-title #general-contribuir }

    ---

    Pensado para que la comunidad pueda remitir incidencias y participar en discusiones sobre la implementación técnica de la NTI-RISP y su evolución a DCAT-AP-ES.

    [:octicons-arrow-right-24: Contribuir](https://github.com/datosgobes/NTI-RISP?tab=readme-ov-file#contribución "Informa acerca de incidencias o mejoras del perfil NTI-RISP")

-   :fontawesome-brands-creative-commons:{ .lg .middle .grid-emoji } **Código abierto, CC-BY 4.0**{ .grid-title #general-license }  

    ---

    Todo el material esta licenciado con la licencia abierta *Creative Commons Attribution 4.0 International*. 

    [:octicons-arrow-right-24: Licencia](https://github.com/datosgobes/NTI-RISP#CC-BY-4.0-1-ov-file "Licencia de uso libre que permite compartir, copiar, distribuir y modificar una obra, incluso con fines comerciales, con la única condición de reconocer la autoría original")

</div>

---