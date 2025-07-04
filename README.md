# ﻿Multilingual Text-to-Image Generation with Semantic Consistency

> **Project Goal**  
Enhance **Stable Diffusion** to accept **multilingual prompts** (Urdu, Arabic, Chinese, Spanish) while preserving **semantic meaning** across translations and generating aligned, coherent images.

---

### 🔧 Day 1: Setup & Kickoff
- ✅ Kickoff meeting and team role distribution
- 🛠️ Installed environment: `Python`, `PyTorch`, `HuggingFace`, `LaBSE`, `XLM-R`
- 📚 Reviewed multilingual models:
  - [LaBSE](https://huggingface.co/sentence-transformers/LaBSE)
  - [XLM-R](https://huggingface.co/xlm-roberta-base)

---

### 🌐 Day 2: Dataset & Translation
- 📥 Loaded small subset of **MS-COCO** captions
- 🌍 Translated to 4 languages: Urdu, Arabic, Chinese, Spanish
- 🗃️ Created multilingual dataset structure:
```json
{
  "image": "image_id.jpg",
  "en_caption": "A dog playing in the park.",
  "lang_caption": {
    "ur": "...",
    "ar": "...",
    "zh": "...",
    "es": "..."
  }
}
```

---

### 🔤 Day 3: Tokenization Analysis
- 🔍 Investigated tokenization differences across languages
- 🧪 Used transformers tokenizer for XLM-R
- 📈 Logged token counts for comparative analysis

---

### 🧠 Day 4: Embedding Alignment
- 📐 Generated sentence embeddings using LaBSE
- 🧮 Computed cosine similarity between English and translated captions
- 📚 Resource: scikit-learn cosine similarity

---

### 📊 Day 5: Embedding Visualization
- 🧬 Applied t-SNE to visualize multilingual sentence embeddings
- 📌 Observed clustering trends and alignment across languages
- 📘 Guide: scikit-learn t-SNE

---

### 🧪 Day 6: Stable Diffusion Pipeline
- ⚙️ Set up Stable Diffusion baseline pipeline
- 🖼️ Generated images from:
    - English prompt
    - Corresponding translated prompts
- 🔄 Compared output to check visual alignment across languages

---

### 📢 Day 7: Internal Presentation & Report
- 🎤 Presented:
    - Data pipeline
    - LaBSE embeddings
    - t-SNE visualizations
    - Translation similarity scores
- 📄 Compiled and submitted detailed report

---
---

### 📌 Key Tools & Resources
| Category      | Tool/Link                                                                                       |
| ------------- | ----------------------------------------------------------------------------------------------- |
| Translation   | [googletrans](https://py-googletrans.readthedocs.io/en/latest/)                                 |
| Tokenization  | [HuggingFace Tokenizers](https://huggingface.co/docs/transformers/tokenizer_summary)            |
| Embeddings    | [LaBSE](https://huggingface.co/sentence-transformers/LaBSE)                                     |
| Visualization | [t-SNE (sklearn)](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html) |
| Text-to-Image | [Stable Diffusion](https://huggingface.co/CompVis/stable-diffusion)                             |
