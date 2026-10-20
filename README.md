# MediLLaMA: AI-Driven Simplification and Multilingual Translation of Medical Reports

MediLLaMA is a research project exploring how clinical information can be made easier for patients to understand and translated into a target language. The workflow combines clinical named-entity recognition, large language model-based simplification, and neural machine translation.

## Research overview

Medical reports often contain technical terminology and complex sentence structures that can be difficult for patients to interpret. MediLLaMA explores a pipeline for transforming clinical text into simpler language and translating that simplified text while aiming to preserve medically important information.

### Workflow

1. **Clinical text preprocessing** — prepare and normalize the source text.
2. **Named-entity recognition (NER)** — identify clinically important terms and entities.
3. **Medical text simplification** — use LLaMA-3 to rewrite complex medical language in a more accessible form.
4. **Translation** — use NLLB-200 to translate the simplified text; Tamil is used as the target language in the implementation.
5. **Evaluation** — assess generated text using overlap-based and translation/simplification metrics.

### Technologies explored

- Python
- Hugging Face Transformers
- LLaMA-3 via the OpenRouter API
- NLLB-200
- BERT-based named-entity recognition
- PEFT/LoRA fine-tuning
- NLTK and text-evaluation metrics
- Google Colab

## Reported evaluation

The research reports the following scores:

| Metric | Reported score |
|---|---:|
| ROUGE-1 | 0.7778 |
| ROUGE-2 | 0.6250 |
| ROUGE-L | 0.7778 |
| BLEU | 0.59 |
| METEOR | 0.3908 |
| Length Ratio | 1.2333 |
| Character Length Ratio | 1.0942 |
| Character Overlap Score | 0.8913 |

These are values reported by the project research, not independently reproduced benchmarks. Metrics depend on the evaluation data and setup.

## Repository contents

- `MediLLaMA_Implementation.ipynb` — notebook containing the prototype workflow.
- `requirements.txt` — Python package dependencies.
- `.gitignore` — excludes common local and generated files from Git tracking.
- `LICENSE` — states the repository's reuse terms.

The full research paper PDF is intentionally not included in this public repository. This README provides a high-level description of the research and implementation.

## Running the notebook

The notebook was prepared for Google Colab and may require changes to paths and runtime configuration.

1. Open the notebook in Google Colab.
2. Provide the dataset expected by the notebook. The current notebook expects a CSV named `medi_translate.csv` with columns `Text`, `Translation`, and `Language`; the Tamil filter expects `Tamil / தமிழ்`.
3. Configure `OPENROUTER_API_KEY` securely through Colab Secrets or an environment variable. Never commit API keys.
4. Review Google Drive paths and dataset access before running cells.
5. Run cells in order. Model downloads and fine-tuning may require substantial RAM and GPU resources.

## Important notes

- The dataset is not included in this repository. Use only data you are authorized to access and share.
- The notebook contains environment-specific assumptions that may need to be adapted.
- This is a research prototype, not a medical device. Generated summaries and translations require qualified review before any clinical use.
- Do not upload identifiable patient information, credentials, API keys, or private datasets.
- Third-party models, libraries, and datasets remain subject to their own licenses and terms.

## Authors

- Mrinal Ashwith S P
- Yuvan Kalyan U
- Hariharan P
- Dr. Suja Golden Shiny S

Please respect the rights of all contributors and obtain permission from the relevant copyright holders before reusing project materials.
