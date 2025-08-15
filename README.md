# PAVE-BR Golden Dataset

**PAVE-BR Golden Dataset** is a manually curated benchmark dataset for **Product Attribute Value Extraction (PAVE)** in the context of Brazilian e-commerce. It is designed to support the evaluation of Large Language Model (LLM)-based extraction systems for Portuguese, and serves as a foundation for the AI-PAVE-Br project. This dataset aims to foster reproducible research in Natural Language Processing (NLP), with a particular focus on product classification and attribute extraction.

---

## Objective

The PAVE-BR Golden Dataset serves as a gold-standard benchmark for evaluating the accuracy and performance of automatic systems in product classification and attribute extraction. By comparing model outputs against expert-annotated ground truth labels, researchers can assess the effectiveness of their approaches using consistent and objective criteria. The dataset has also been used to benchmark the proposed AI-PAVE-Br model against traditional and LLM-based baselines.

---

## Dataset Formats
The dataset is available in two formats:
* **Excel format** (`Dataset_in_Excel`)

  * Each sheet corresponds to a specific product category.
  * May include visual annotations (e.g., color coding) to support review and validation.

* **CSV format** (`Dataset_in_CSVs`)

  * Each product category is represented by a separate CSV file.
  * This structure avoids excessive sparsity, as each category has a distinct attribute schema that would otherwise result in large numbers of missing values in a unified format.

---

## Scope and Construction

All annotations were produced manually by a trained annotation team, with close attention to the specific linguistic and contextual nuances of Brazilian e-commerce. The dataset supports evaluation for both product classification (entity-level) and attribute extraction tasks.

### Product Types Included

The dataset includes representative and high-impact product types from Brazilian e-commerce, such as:

> Air Conditioner, TV, Cell Phone, Refrigerator, Notebook, Tire, Wardrobe, Bed, Sneaker, Stove, Table and Chair Set, Backpack, Faucet, Headphone, Perfume, Doll, Motorcyclist Helmet, Pot, Lamp, Cell Phone Case.

---

## Annotation Schema

Each annotated product includes:

* **Entity (Tipo de Produto):** The most specific product type (e.g., 'Ar Condicionado', 'Perfume').
* **Category (Categoria):** A broader classification group (e.g., 'AR' for air conditioners).
* **Subcategories (Subcategoria):** A list of relevant domain-specific tags or subcategories (e.g., `['ARCA', 'ACIV', 'ARAR']` for an air conditioner).

The annotation schema was defined in advance, and the list of attributes per product type was determined based on domain expertise and platform conventions.

Refer to *Table 1. Product Entities and Their Associated Attribute Lists* in the accompanying paper for a complete specification of attributes per product type.

---

## Sampling Methodology

To ensure statistical robustness and reduce selection bias, products were sampled randomly from each product type, considering their platform-level classification. Sample sizes were determined using **Cochran’s formula** for large populations, targeting a 95% confidence level with a 5% margin of error. This led to approximately **385 annotated items per product type**, balancing statistical validity with the practical limitations of manual annotation effort.

---

## License

This dataset is released under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)** license.

You are free to:

* **Share** — copy and redistribute the material in any medium or format.
* **Adapt** — remix, transform, and build upon the material.

Under the following terms:

* **Attribution (BY)** — You must give appropriate credit to Magazine Luiza, provide a link to the license, and indicate if changes were made.
* **NonCommercial (NC)** — You may not use the material for commercial purposes.
* **ShareAlike (SA)** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license.

For the full legal terms, please refer to the [LICENSE](LICENSE) file.

---

## Citation

If you use the PAVE-BR Golden Dataset in your research, please cite it as follows (or use the `CITATION.cff` file included in the repository):

> Gazzola, M., Souto, H. G., Silva, S., Peixoto, J. S., Siqueira, F., Morais, A. L. P., & Gomes, C. (2025).
AI-PAVE-Br: Leveraging Large Language Models for Enhanced Product Attribute Value Extraction through a Golden Set Approach.
In Proceedings of the Symposium in Information and Human Language Technology (STIL 2025).

```bibtex
@inproceedings{gazzola2025aipavebr,
  author    = {Murilo Gazzola and Hugo Gobato Souto and Samuel Silva and Júlia Schubert Peixoto and Felipe Siqueira and André Luis Pedroso de Morais and Caio Gomes},
  title     = {AI-PAVE-Br: Leveraging Large Language Models for Enhanced Product Attribute Value Extraction through a Golden Set Approach},
  booktitle = {Proceedings of the Symposium in Information and Human Language Technology (STIL)},
  year      = {2025},
  url       = {https://github.com/ai-luizalabs/AI-PAVE-Br}
}

