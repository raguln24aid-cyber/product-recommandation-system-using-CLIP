# Gen AI Bootcamp Day 2 — AI Product Intelligence

This repository contains the finished notebook [gen_ai_bootcamp_day2-solution.ipynb](gen_ai_bootcamp_day2-solution.ipynb) which builds a small AI product-intelligence system using CLIP + FAISS.

## Summary
- Tasks:
  - Task 1 — Smart complementary product recommendations
  - Task 2 — Unique product catalog (dedup) via clustering
  - Task 3 — Reverse text → product search
- Key components / symbols (see notebook for implementation):
  - Data paths: [`DATASET_BASE`](gen_ai_bootcamp_day2-solution.ipynb), [`IMAGES_DIR`](gen_ai_bootcamp_day2-solution.ipynb), [`CSV_PATH`](gen_ai_bootcamp_day2-solution.ipynb)
  - Embedding helpers: [`get_image_embedding`](gen_ai_bootcamp_day2-solution.ipynb), [`get_text_embedding`](gen_ai_bootcamp_day2-solution.ipynb)
  - Index & vectors: [`embeddings`](gen_ai_bootcamp_day2-solution.ipynb), [`emb_normed`](gen_ai_bootcamp_day2-solution.ipynb), [`index`](gen_ai_bootcamp_day2-solution.ipynb)
  - Recommendation logic: [`COMPLEMENTARY_RULES`](gen_ai_bootcamp_day2-solution.ipynb), [`get_complementary_categories`](gen_ai_bootcamp_day2-solution.ipynb), [`recommend_complementary`](gen_ai_bootcamp_day2-solution.ipynb)
  - Catalog / clustering: [`DISTANCE_THRESHOLD`](gen_ai_bootcamp_day2-solution.ipynb), [`get_cluster_representative`](gen_ai_bootcamp_day2-solution.ipynb), [`labels`](gen_ai_bootcamp_day2-solution.ipynb), [`catalog_df`](gen_ai_bootcamp_day2-solution.ipynb), [`df_valid`](gen_ai_bootcamp_day2-solution.ipynb)
  - Text search & viz: [`text_to_product_search`](gen_ai_bootcamp_day2-solution.ipynb), [`visualize_recommendations`](gen_ai_bootcamp_day2-solution.ipynb), [`visualize_text_search`](gen_ai_bootcamp_day2-solution.ipynb)

## Requirements
- Python 3.11+
- Libraries (notebook installs): transformers, torch, torchvision, Pillow, scikit-learn, matplotlib, seaborn, pandas, numpy, faiss-cpu, tqdm

## Quickstart
1. Open the notebook: [gen_ai_bootcamp_day2-solution.ipynb](gen_ai_bootcamp_day2-solution.ipynb)
2. Ensure dataset path variables [`DATASET_BASE`](gen_ai_bootcamp_day2-solution.ipynb), [`IMAGES_DIR`](gen_ai_bootcamp_day2-solution.ipynb), [`CSV_PATH`](gen_ai_bootcamp_day2-solution.ipynb) point to your data.
3. Run cells top-to-bottom. Notebook stages:
   - Install & import libs
   - Load dataset & sample images
   - Load CLIP model and generate embeddings (`[`get_image_embedding`](gen_ai_bootcamp_day2-solution.ipynb)`, `[`get_text_embedding`](gen_ai_bootcamp_day2-solution.ipynb)`)
   - Build FAISS index and run Task 1, Task 2, Task 3 visualizations

## Notes
- Cosine-based clustering uses distance = $1 - \cos(\theta)$ (see clustering cell).  
- The notebook contains visualization and CSV export of the deduplicated catalog.

## Useful links
- Notebook: [gen_ai_bootcamp_day2-solution.ipynb](gen_ai_bootcamp_day2-solution.ipynb)
- Referenced helpers and cells: see the symbol links above in this file (all point to the notebook).

## License
Use as-is for learning / internal demos.
