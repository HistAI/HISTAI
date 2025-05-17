# HISTAI - A Whole Slide Images Pathology Dataset

HISTAI is a comprehensive, open-source Whole Slide Image (WSI) dataset designed to advance research and development in digital pathology. It provides a diverse, multimodal, and richly annotated collection comprising over 60,000 slides from multiple organ systems and pathological specializations. Each slide includes extensive clinical, pathological, and technical metadata, enabling a wide range of research applications from diagnostic modeling to multimodal analyses.

---

## 🔗 Access the Dataset

* **Metadata Repository:** [HISTAI-metadata](https://huggingface.co/datasets/histai/HISTAI-metadata) [START HERE]
* **Individual Specialized Subsets:**

  * [HISTAI-hematologic](https://huggingface.co/datasets/histai/HISTAI-hematologic)
  * [HISTAI-gastrointestinal](https://huggingface.co/datasets/histai/HISTAI-gastrointestinal)
  * [HISTAI-breast](https://huggingface.co/datasets/histai/HISTAI-breast)
  * [HISTAI-thorax](https://huggingface.co/datasets/histai/HISTAI-thorax)
  * [HISTAI-skin-b2](https://huggingface.co/datasets/histai/HISTAI-skin-b2)
  * [HISTAI-skin-b1](https://huggingface.co/datasets/histai/HISTAI-skin-b1)
  * [HISTAI-colorectal-b1](https://huggingface.co/datasets/histai/HISTAI-colorectal-b1)
  * [HISTAI-colorectal-b2](https://huggingface.co/datasets/histai/HISTAI-colorectal-b2)

---

## 📄 Paper and Citation

A detailed research paper describing the HISTAI dataset is available:

**HISTAI: An Open-Source, Large-Scale Whole Slide Image Dataset for Computational Pathology**

\[📌 Paper Coming Soon]

---

## 📂 Dataset Structure

Slides are organized by cases within specialized subsets following this naming convention:

```
histai/<dataset_name>/case_<case_id>/slide_<stain>_<slide_number>.tiff
```

or

```
histai/<dataset_name>/case_<case_id>/slide_<magnification>_<stain>_<slide_number>.tiff
```

* **Standard magnification:** 20X (explicitly mentioned if differs)
* **Staining:** Primarily Hematoxylin and Eosin (H\&E)
* **Scanners used:** Primarily Leica Aperio GT450, AT2, some Hamamatsu, and 3DHISTECH systems.

---

## 📋 Metadata

Detailed metadata accompanies each slide, provided in JSON format. Fields include:

| Field             | Description                               | Example                                              |
| ----------------- | ----------------------------------------- | ---------------------------------------------------- |
| `diagnosis`       | Clinical diagnostic notes                 | Benign skin neoplasms                                |
| `conclusion`      | Pathological conclusions                  | Intradermal melanocytic nevus                        |
| `diff_diagnosis`  | Differential diagnostic notes             |                                                      |
| `micro_protocol`  | Microscopic examination details           | Intradermal melanocytic nevus of the skin            |
| `additional_info` | Supplementary clinical/pathological notes | "Repeat review of histological specimens..."         |
| `age`             | Patient age (years)                       | 37                                                   |
| `gender`          | Patient gender                            | f                                                    |
| `icd10`           | ICD-10 codes                              | D22                                                  |
| `specialization`  | Medical specialization or organ system    | Skin                                                 |
| `case_mapping`    | References to slide images                | histai/HISTAI-skin-b2/case\_13384                    |
| `grossing`        | Gross examination details                 | "Head and neck: One fragment, 2×4 mm, gray, firm..." |

---

## 📊 Dataset Statistics

| Dataset                 | Total Slides | Total Cases |
| ----------------------- | -----------: | ----------: |
| HISTAI-hematologic      |          214 |         214 |
| HISTAI-gastrointestinal |          202 |         120 |
| HISTAI-breast           |        1,925 |       1,692 |
| HISTAI-thorax           |          829 |         657 |
| HISTAI-skin-b2          |       43,757 |      20,621 |
| HISTAI-skin-b1          |        7,710 |       1,778 |
| HISTAI-colorectal-b1    |        5,379 |         998 |
| HISTAI-colorectal-b2    |           94 |          62 |

**Total slides**: 60,110
**Total cases**: 26,142
**Magnification:** 20X (57,647 slides), 40X (2,463 slides)
**Stains:** H\&E (58,282 slides), Other (1,828 slides)

---

## 🛠️ How to Download

### Using Hugging Face Hub

```python
from huggingface_hub import snapshot_download

snapshot_download(repo_id="histai/<dataset_name>", repo_type="dataset", local_dir="/local_path")
```

### Using Git

```bash
git lfs install
git clone https://huggingface.co/datasets/histai/<dataset_name>
```

---

## 🔖 License

The HISTAI dataset is licensed under **CC BY-NC 4.0** and intended for research purposes only.

---

## 📌 Checkout Our Other Repositories

* [**SPIDER**](https://github.com/HistAI/SPIDER): A multi-organ supervised pathology dataset with patch-level annotations and pretrained baseline models.
* [**Hibou**](https://github.com/HistAI/hibou): Foundational vision models optimized for digital pathology tasks.

---

## 📧 Contact

**Authors:** Dmitry Nechaev, Alexey Pchelnikov, Ekaterina Ivanova
**Emails:** [dmitry@hist.ai](mailto:dmitry@hist.ai), [alex@hist.ai](mailto:alex@hist.ai), [kate@hist.ai](mailto:kate@hist.ai)
