# MediLLaMA: AI-Driven Simplification and Multilingual Translation of Medical Reports

MediLLaMA is a research project focused on simplifying complex medical reports and translating clinical information into regional languages to improve patient accessibility and understanding. The approach combines clinical Named Entity Recognition (NER), Large Language Models (LLMs) for medical text simplification, and neural machine translation.

## Publication Details

**Research Publication:** MediLLaMA: AI-Driven Simplification and Multilingual Translation of Medical Reports

**Authors:**
- Mrinal Ashwith S P
- Yuvan Kalyan U
- Hariharan P
- Dr. Suja Golden Shiny S

**Conference:** 2026 IEEE International Conference on Communication, Information and Smart Systems Development (ICCISD)

**Publisher:** IEEE

**DOI:** [10.1109/ICCISD69924.2026.11732006](https://doi.org/10.1109/ICCISD69924.2026.11732006)

The publication investigates an AI-driven pipeline for transforming complex clinical language into more accessible text while supporting multilingual communication. The full research paper is intentionally not included in this repository.

## Research Overview

Medical reports frequently contain specialized terminology, complex sentence structures, and clinical abbreviations that can be difficult for patients to understand. Language barriers can further limit access to essential healthcare information.

MediLLaMA explores a hybrid NLP pipeline that combines medical entity recognition, LLM-based simplification, and neural machine translation to make clinical information more accessible while aiming to preserve medically important details.

## Proposed Workflow

1. **Clinical Text Preprocessing:** Clean and normalize medical text for downstream processing.
2. **Named Entity Recognition (NER):** Identify clinically important entities and terminology.
3. **Medical Text Simplification:** Apply LLaMA-3 to rewrite complex medical language into more accessible explanations.
4. **Multilingual Translation:** Use NLLB-200 to translate simplified text, with Tamil as the target language in the implementation.
5. **Evaluation:** Assess generated outputs using text-overlap, simplification, and translation evaluation metrics.

## Technologies and Frameworks

- **Programming:** Python
- **Large Language Models:** LLaMA-3
- **Machine Translation:** NLLB-200
- **Natural Language Processing:** BERT-based Named Entity Recognition
- **Model Fine-Tuning:** PEFT and LoRA
- **Deep Learning:** PyTorch and Hugging Face Transformers
- **Evaluation:** ROUGE, BLEU, METEOR, and character-overlap metrics
- **API Integration:** OpenRouter API
- **Development Environment:** Google Colab

## Reported Evaluation Results

The research reports the following evaluation scores:

| Metric | Reported Score |
|---|---:|
| ROUGE-1 | 0.7778 |
| ROUGE-2 | 0.6250 |
| ROUGE-L | 0.7778 |
| BLEU | 0.5900 |
| METEOR | 0.3908 |
| Length Ratio | 1.2333 |
| Character Length Ratio | 1.0942 |
| Character Overlap Score | 0.8913 |

These values are reported results from the research. They should be interpreted in the context of the evaluation dataset, reference texts, and experimental configuration.

## Repository Contents

- `MediLLaMA_Implementation.ipynb` — implementation notebook for the research workflow.
- `requirements.txt` — Python dependencies.
- `.gitignore` — excludes selected local files and generated artifacts from Git tracking.
- `LICENSE` — repository usage and copyright notice.

The complete research paper is not hosted in this repository. Publication metadata and the DOI are provided above for academic reference.

## Running the Implementation

The implementation notebook was prepared primarily for Google Colab.

1. Open `MediLLaMA_Implementation.ipynb` in Google Colab.
2. Configure the required dataset and verify the expected CSV filename, column names, and language labels.
3. Configure the OpenRouter API key securely using Colab Secrets or environment variables.
4. Review notebook paths and Google Drive dependencies.
5. Install the required packages and execute the notebook cells in order.

Model downloads, fine-tuning, and inference may require substantial memory and GPU resources.

## Important Notes

- The dataset is not included in this repository.
- Dataset access, model availability, and third-party licenses remain subject to their respective terms.
- The notebook may require environment-specific configuration before execution.
- MediLLaMA is a research prototype, not a clinically validated medical device. Generated summaries and translations require appropriate professional review before clinical use.
- Do not upload identifiable patient information, confidential datasets, API keys, or other sensitive information.

## Authors and Acknowledgements

This research was conducted by Mrinal Ashwith S P, Yuvan Kalyan U, Hariharan P, and Dr. Suja Golden Shiny S.

Please refer to the publication DOI for the research record and citation information.

## Copyright and Usage

Copyright and reuse rights remain subject to the applicable rights of the authors, contributors, and third-party component owners.

No permission is granted to reuse project materials beyond the rights expressly provided by the applicable license or copyright holder. Please obtain appropriate permission before reproducing or redistributing protected materials.
