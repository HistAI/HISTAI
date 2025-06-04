HISTAI - A Whole Slide Images Pathology Dataset

HISTAI is a comprehensive, open-source Whole Slide Image (WSI) dataset designed to advance research and development in digital pathology. It provides a diverse, multimodal, and richly annotated collection comprising over 112,000 slides from multiple organ systems and pathological specializations. Each slide includes extensive clinical, pathological, and technical metadata, enabling a wide range of research applications from diagnostic modeling to multimodal analyses.

If you wish to support, sponsor, or obtain a commercial license for HISTAI data, please contact us at [models@hist.ai](mailto:models@hist.ai).

⸻

🔗 Access the Dataset
	•	Metadata Repository: HISTAI-metadata [START HERE]
	•	Individual Specialized Subsets:
	•	HISTAI-hematologic
	•	HISTAI-gastrointestinal
	•	HISTAI-breast
	•	HISTAI-thorax
	•	HISTAI-skin-b2
	•	HISTAI-skin-b1
	•	HISTAI-colorectal-b1
	•	HISTAI-colorectal-b2
	•	HISTAI-mixed

⸻

📄 Paper and Citation

A detailed research paper describing the HISTAI dataset is available:

HISTAI: An Open-Source, Large-Scale Whole Slide Image Dataset for Computational Pathology
Dmitry Nechaev, Alexey Pchelnikov, Ekaterina Ivanova
📖 Read on arXiv

📚 Citation

If you use HISTAI in your research, please cite:

@misc{nechaev2025histaiopensourcelargescaleslide,
  title     = {HISTAI: An Open-Source, Large-Scale Whole Slide Image Dataset for Computational Pathology},
  author    = {Dmitry Nechaev and Alexey Pchelnikov and Ekaterina Ivanova},
  year      = {2025},
  eprint    = {2505.12120},
  archivePrefix = {arXiv},
  primaryClass  = {eess.IV},
  url       = {https://arxiv.org/abs/2505.12120}
}


⸻

📂 Dataset Structure

Slides are organized by cases within specialized subsets following this naming convention:

histai/<dataset_name>/case_<case_id>/slide_<stain>_<slide_number>.tiff

or

histai/<dataset_name>/case_<case_id>/slide_<magnification>_<stain>_<slide_number>.tiff

	•	Standard magnification: 20X (explicitly mentioned if differs)
	•	Staining: Primarily Hematoxylin and Eosin (H&E)
	•	Scanners used: Primarily Leica Aperio GT450, AT2, some Hamamatsu, and 3DHISTECH systems.

⸻

📋 Metadata

Detailed metadata accompanies each slide, provided in JSON format. Fields include:

Field	Description	Example
diagnosis	Incoming clinical notes	Benign skin neoplasms
conclusion	Final pathological conclusion	Intradermal melanocytic nevus of the skin
diff_diagnosis	Differential diagnostic notes (if available)	
micro_protocol	Microscopic description	Skin: Intradermal melanocytic nevus
additional_info	Supplementary clinical/pathological notes	“A repeat review of histological specimens was performed…”
age	Patient age (years)	37
gender	Patient gender	f
icd10	ICD-10 codes	D22
specialization	Medical specialization or organ system	Skin
case_mapping	References to slide images	histai/HISTAI-skin-b2/case_13384
grossing	Gross examination details	“Head and neck: One fragment, 2×4 mm, gray, firm…”


⸻

📊 Dataset Statistics

Dataset	Total Slides	Total Cases
HISTAI-hematologic	214	214
HISTAI-gastrointestinal	202	120
HISTAI-breast	1,925	1,692
HISTAI-thorax	829	657
HISTAI-skin-b2	43,757	20,621
HISTAI-skin-b1	7,710	1,778
HISTAI-colorectal-b1	5,379	998
HISTAI-colorectal-b2	94	62
HISTAI-mixed	52,691	21,137

Total slides: 112,801
Total cases: 47,279
Magnification: 20X (110,338 slides), 40X (2,463 slides)
Stains: H&E (92,536 slides), IHC (16,920 slides), Other (3,345 slides)

⸻

🛠️ How to Download

Using Hugging Face Hub

from huggingface_hub import snapshot_download

snapshot_download(repo_id="histai/<dataset_name>", repo_type="dataset", local_dir="/local_path")

Using Git

git lfs install
git clone https://huggingface.co/datasets/histai/<dataset_name>


⸻

🔖 License

The HISTAI dataset is licensed under CC BY-NC 4.0 and intended for research purposes only. For commercial use, contact models@hist.ai.

⸻

📌 Checkout Our Other Repositories
	•	SPIDER: Multi-organ supervised dataset with annotations.
	•	Hibou: Vision models for digital pathology.

⸻

📧 Contact

Authors: Dmitry Nechaev, Alexey Pchelnikov, Ekaterina Ivanova
Emails: dmitry@hist.ai, alex@hist.ai, kate@hist.ai
