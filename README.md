# 📚 AI-Based Peer Tutor Matcher

An intelligent peer tutoring matching system using Graph Neural Networks (GraphSAGE) and knowledge graphs to connect students with appropriate tutors.

## 📓 Notebook Overview

This repository contains `train_model.ipynb` - a complete Jupyter notebook that implements the entire pipeline:

1. **Setup & Installation** - Installs required libraries (PyTorch, PyTorch Geometric, Neo4j, etc.)
2. **Data Loading** - Loads student performance dataset (1,194 students, 32 attributes)
3. **Data Preprocessing** - Cleans columns, handles missing values, encodes categorical variables
4. **Role Assignment** - Classifies students as Tutors (CGPA ≥ 3.0 & no probation) or Tutees
5. **Feature Engineering** - Creates 22-dimensional feature vectors
6. **Neo4j Graph Construction** - Builds knowledge graph with students as nodes and POTENTIAL_MATCH edges
7. **GraphSAGE Training** - Trains GNN model with link prediction objective (50 epochs)
8. **Visualization** - Feature matrix heatmaps and training accuracy plots
9. **Model Export** - Saves trained model (`graphsage_model.pt`) and features (`features.pkl`)

## 🚀 Running the Notebook

### Prerequisites

```bash
pip install torch torchvision torchaudio torch-geometric pandas numpy openpyxl scikit-learn matplotlib seaborn neo4j

Steps
Open train_model.ipynb in Jupyter Notebook/Google Colab

Run cells sequentially

Upload the student dataset when prompted

Update Neo4j credentials (create free AuraDB instance if needed)

Train the model and download the output files

📊 Key Results
Test Accuracy: 49.66%

Students: 1,194 (704 Tutors, 490 Tutees)

Graph Edges: 344,960 POTENTIAL_MATCH relationships

Embedding Size: 32 dimensions

📁 Files in this Repository
File	Description
train_model.ipynb	Complete training pipeline notebook
README.md	Project documentation
🔧 Technologies Used
Python

PyTorch & PyTorch Geometric

GraphSAGE

Neo4j

pandas, numpy, scikit-learn

matplotlib, seaborn

👨‍💻 Author
Rehan Ali - NUM-BSCS-2023-15
Namal University, Mianwali, Pakistan
Email: bscs23f15@namal.edu.pk

Supervisor: Dr. Shafiq Ur Rehman Khan
