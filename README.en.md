# NTI-RISP Repository
[![EN](https://img.shields.io/badge/lang-EN-blue.svg)](README.en.md) [![ES](https://img.shields.io/badge/lang-ES-yellow.svg)](README.md)

This project provides a set of resources for the [technical implementation of NTI-RISP (2013)](https://datos.gob.es/es/documentacion/etiquetas/normativas-3836), an application profile of the Data Catalog Vocabulary for Spain.

> [!TIP]
> The documentation available at [NTI-RISP Online](https://datosgobes.github.io/NTI-RISP/) is intended to serve as a reference for both publishers and users of open data. It details the principles and guidelines for structuring and describing datasets according to the [Norma Técnica de Interoperabilidad de Reutilización de Recursos de Información (NTI-RISP)](https://www.boe.es/eli/es/res/2013/02/19/(4)) metadata model, facilitating their interoperability and reuse. It also includes metadata schemas, practical examples, and implementation guidance to help ensure correct adoption of the profile.

## Project Structure

The project is organized as follows:

- `.devcontainer`: Configuration for [Dev Containers](https://containers.dev/implementors/spec/), a feature that allows development in a pre-configured environment within a [Docker](https://docs.docker.com/) container.
- `.github/workflows/`: Contains [GitHub Actions](https://docs.github.com/en/actions) workflows for generating the online documentation.
- `docs/`: Main project documentation in [`Markdown`](https://daringfireball.net/projects/markdown/syntax) format for [MKDocs](https://www.mkdocs.org/getting-started/).
- `overrides`: [Custom templates](https://squidfunk.github.io/mkdocs-material/customization/) for the online documentation.
- `examples/`: Usage examples of `NTI-RISP`.
- `refs/`: Additional references and related documentation.
- `tools/`: Tools and useful software for project management.

## Contribution

If you want to contribute to this project, for example by fixing a [SHACL validation file](https://datos.gob.es/en/blog/shacl-un-lenguaje-para-validar-grafos-rdf) of `NTI-RISP`, please follow these steps:

1. Fork the [`datosgobes/NTI-RISP`](https://github.com/datosgobes/NTI-RISP) repository.

    ```sh
    git clone https://github.com/datosgobes/NTI-RISP.git
    ```

2. Create a new branch with your fix

    ```sh
    git checkout -b fix/shacl-property-x
    ```

3. Make your changes and commit them:

    ```sh
    git commit -am 'Fixed range of property x'
    ```

4. Push your changes:

    ```sh
    git push origin fix/shacl-property-x
    ```

5. To commit the change to the main branch, open a Pull Request(https://github.com/datosgobes/NTI-RISP/pulls).

## Development  

To preview the documentation with MkDocs and launch it in debug mode, check the following documentation: [Information about MkDocs](./refs/dev/mkdocs.md).  

### Translation  

This documentation uses [`mkdocs-static-i18n`](https://ultrabug.github.io/mkdocs-static-i18n/) to support multiple languages. To achieve this, the suffix structure is adopted:  

```bash
├── assets
│   ├── css
│   └── js
├── img
├── conventions.en.md
├── conventions.md
├── examples.en.md
├── examples.md
├── index.md
└── robots.txt
```

> [!NOTE]  
> When using the suffix structure for documentation files (default), you must add the suffix `.<language>.<extension>` to your files (e.g., `index.en.md`).  
> More information at: [MkDocs static i18n plugin documentation](https://ultrabug.github.io/mkdocs-static-i18n/getting-started/quick-start/)

## License

All material in this repository is published under the licence `CC-BY 4.0`, unless explicitly otherwise mentioned. See the [LICENSE](./LICENSE) file for more details.

## Contact

For any questions or suggestions, please [open an Issue in the repository](https://github.com/datosgobes/NTI-RISP/issues) or contact the project maintainers.