# phytoplankton-image-retrieval
Image-based phytoplankton identification using vector embeddings and similarity search (Qdrant + CLIP)

## License

This project is released under the Apache License 2.0.

# Phytoplankton Image Retrieval

This project implements an **image-based retrieval system for phytoplankton identification** using deep visual embeddings and a vector database.

The system allows a user to upload a phytoplankton image and retrieve the most visually similar samples from a reference database, enabling **genus inference** and access to **domain-specific properties** in a transparent and explainable way.

The project is designed as a **modular, end-to-end AI pipeline**, from data ingestion and embedding generation to similarity search and downstream applications.

---

## Project Goals

- Build a **robust image similarity search system** for phytoplankton images  
- Enable **genus identification** using visual similarity (kNN-based baseline)  
- Provide **interpretable results** instead of black-box predictions  
- Serve as a **reference implementation** for computer vision + vector databases  
- Demonstrate applied AI engineering practices  

---

## High-Level Architecture

1. **Image ingestion**
   - Load phytoplankton images and metadata (genus labels)
2. **Embedding generation**
   - Generate visual embeddings using a pre-trained CLIP model
3. **Vector storage**
   - Store embeddings and metadata in a Qdrant vector database
4. **Similarity search**
   - Retrieve top-k most similar images for a query image
5. **Inference layer**
   - Infer the most likely genus using kNN voting
6. **Application layer (planned)**
   - User-facing app for image upload and result visualization

---

## Repository Structure

phytoplankton-image-retrieval/
├─ README.md
├─ requirements.txt
├─ docker-compose.yml
├─ configs/
│ └─ config.yaml
├─ data/
│ ├─ README.md
│ └─ sample_metadata.csv
└─ src/
├─ ingest.py
├─ utils.py
└─ (future modules: search, app, evaluation)
