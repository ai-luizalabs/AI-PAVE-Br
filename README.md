# PAVE-BR-Golden-Dataset 🏆
PAVE-BR Golden Dataset: A meticulously curated, manually annotated dataset for Product Attribute Value Extraction (PAVE) in Brazilian e-commerce 🇧🇷. Designed to benchmark LLM-based 🤖 PAVE for Portuguese, supporting the AI-PAVE-Br project and fostering reproducible NLP research.

## Purpose of the Golden Set 🎯

The PAVE-BR Golden Dataset acts as an objective benchmark for evaluating the quality and performance of AI models in product classification and attribute extraction. By comparing model predictions against the expert-annotated labels in this dataset, researchers and developers can quantitatively assess model accuracy without relying on subjective judgments. It is also used for comparing the proposed AI-PAVE-Br model against existing baseline systems.

## Dataset Structure and Formats 📂

The Golden Set is provided in two primary formats:

*   **`Dataset_in_Excel` 📊:**
    *   Contains the complete dataset organized into separate sheets, with each sheet dedicated to a specific product category.
    *   The Excel files may include color-coding 🎨 for additional annotations or information.

*   **`Dataset_in_CSVs` 📜:**
    *   Contains the dataset exported into individual CSV files.
    *   **One CSV file per product category:** This structure is adopted because each product category has unique characteristics and thus requires its own set of columns. Consolidating all data into a single CSV would result in many columns with `NaN` values for most entries, making it less efficient and harder to manage.

## Construction and Scope 🏗️

The annotation of this Golden Set was performed meticulously by a dedicated annotation team, focusing on the specific nuances of Brazilian e-commerce. The dataset is designed to evaluate both product classification and attribute extraction models.

### Selected Product Types: 🛒

Products were strategically chosen to ensure a balanced and representative sample of high-impact items within the Brazilian e-commerce landscape. The dataset includes data for:

Air Conditioner, TV, Cell Phone, Refrigerator, Notebook, Tire, Wardrobe, Bed, Sneaker, Stove, Table and Chair Set, Backpack, Faucet, Headphone, Perfume, Doll, Motorcyclist Helmet, Pot, Lamp, Cell Phone Case.

## Annotation Schema and Data Structure 📝

For each product, the annotation team meticulously labeled the following attributes:

*   **Entity (Tipo de Produto):** The most granular product type (e.g., 'Ar Condicionado', 'Perfume').
*   **Category (Categoria):** The broader product category (e.g., 'AR' for Air Conditioner, 'PF' for Perfume).
*   **Subcategories (Subcategoria):** A list of strings detailing more specific subcategories or attributes relevant to the product (e.g., `['ARCA', 'ACIV', 'ARAR']` for an Air Conditioner).

A clear definition of the list of attributes to be extracted for each product type is essential. The initial annotation wave covered entities and their associated attribute lists, forming the basis for experiments.

*(Refer to `Table 1. Product Entities and Their Associated Attribute Lists` in the accompanying paper for detailed attribute lists per entity.)*

## Sampling Methodology 🎲

Products were sampled randomly while considering existing classifications to ensure statistical validity and reduce selection bias. The sample size for each product type was determined using Cochran's formula for a large population, aiming for a 95% confidence level and a 5% margin of error, with a sample size of approximately 385 items per product type where feasible. This approach balances statistical reliability with project feasibility, given the significant costs of manual annotation.


## 📄 License

The Golden Set dataset is made available under the **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)**.

This means you are free to:
    - **Share** — copy and redistribute the material in any medium or format.
    - **Adapt** — remix, transform, and build upon the material.

Under the following terms:
    - **Attribution (BY)** — You must give appropriate credit to Magazine Luiza, provide a link to the license, and indicate if changes were made.
    - **NonCommercial (NC)** — You may **not** use the material for commercial purposes.
    - **ShareAlike (SA)** — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

For the full license text, please see the [LICENSE](LICENSE) file.

## Citation 📚

If you use the PAVE-BR Golden Dataset in your research, please cite it using the following details (or by referencing the `CITATION.cff` file):