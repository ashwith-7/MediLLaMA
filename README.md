# MediLLaMA: AI-Driven Simplification and Multilingual Translation of Medical Reports

**Research paper and implementation notebook**

MediLLaMA is a clinical NLP workflow designed to make medical discharge reports easier for patients to understand and to translate simplified content into another language. The paper describes a pipeline combining named-entity recognition (NER), LLaMA-3-based simplification, and NLLB-200 translation, with Tamil used as the target language in the implementation.

## Research paper

The full paper is available here:

[`MediLLaMA_Research_Paper.pdf`](MediLLaMA_Research_Paper.pdf)

**Authors**
- Mrinal Ashwith S P
- Yuvan Kalyan U
- Hariharan P
- Dr. Suja Golden Shiny S

## Pipeline

1. **Preprocessing** — clean and normalize clinical text.
2. **Named-entity recognition** — identify important terms in the report.
3. **Medical text simplification** — use LLaMA-3 through the OpenRouter API to rewrite clinical language in patient-friendly terms.
4. **Translation** — use NLLB-200 for English-to-Tamil translation.
5. **Evaluation** — calculate text-overlap and translation/simplification metrics.

## Reported results

The paper reports the following evaluation scores:

| Metric | Score |
|---|---:|
| ROUGE-1 | 0.7778 |
| ROUGE-2 | 0.6250 |
| ROUGE-L | 0.7778 |
| BLEU | 0.59 |
| METEOR | 0.3908 |
| Length Ratio | 1.2333 |
| Character Length Ratio | 1.0942 |
| Character Overlap Score | 0.8913 |

These are the results reported in the accompanying paper; results may vary depending on data, model versions, and evaluation setup.

## Files

- `MediLLaMA_Research_Paper.pdf` — research paper.
- `MediLLaMA_Implementation.ipynb` — notebook for the prototype workflow.

## Run the notebook

The notebook was prepared for **Google Colab** and uses Hugging Face Transformers, Datasets, PEFT/LoRA, NLTK, and the OpenRouter API.

1. Open the notebook in Google Colab.
2. Add your translation dataset as `medi_translate.csv`, or update the notebook's dataset path. The notebook expects columns named `Text`, `Translation`, and `Language`; the Tamil filter currently expects `Tamil / தமிழ்`.
3. Set `OPENROUTER_API_KEY` securely in Colab Secrets (or as an environment variable). Do not paste API keys into notebook cells or commit them to GitHub.
4. Review and update Google Drive paths before running.
5. Run the cells in order. Model downloads and fine-tuning can require substantial RAM, GPU memory, and runtime.

### Important implementation notes

- The dataset is **not included** in this repository. Use data you are authorized to access and share.
- The notebook uses Google Drive paths and Colab-specific imports; adapt them if running elsewhere.
- The paper and notebook may describe different experiment settings. Check the notebook's actual training configuration before attempting to reproduce the paper's reported results.
- This is a research prototype, not a medical device. Generated summaries and translations must be reviewed by qualified professionals before any clinical use.
- Do not upload identifiable patient records, private clinical data, credentials, or API keys to a public repository.

## Technologies

Python · PyTorch · Hugging Face Transformers · NLLB-200 · BERT NER · PEFT/LoRA · NLTK · OpenRouter API · Google Colab

## Citation

If you use or refer to this work, cite the paper using the author and title information on the first page of the PDF. Add publication or DOI details only if/when they are officially available.
