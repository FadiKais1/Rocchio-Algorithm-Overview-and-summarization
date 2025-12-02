
🌟 README.md — Rocchio Relevance Feedback Implementation
Rocchio Algorithm for Query Optimization

This project implements the Rocchio Relevance Feedback Algorithm using a simulated document collection represented with tf-idf features.
The goal is to demonstrate how a query can be improved based on similarity measurements and feedback from relevant and non-relevant documents.

📌 Project Overview

The Rocchio algorithm is a classical method in information retrieval used to refine search queries.
It represents both documents and queries as numeric vectors (using tf-idf) and then adjusts the query so it shifts:

Toward relevant documents

Away from non-relevant documents

In this project we:

✔ Build a vocabulary
✔ Simulate 50 documents with tf-idf-like values
✔ Create an initial query vector
✔ Compute cosine similarity between each document and the query
✔ Select top-relevant and non-relevant documents
✔ Compute the Rocchio vectors:
  - R: average relevant documents
  - R′: strongest relevant documents
  - NR: non-relevant documents

✔ Compute the optimized query vector q(opt)
✔ Rank documents by similarity to q(opt)
✔ Generate detailed views (tables) for each stage

This workflow demonstrates the full information retrieval pipeline using vector space modeling.

🧠 Algorithm Summary

The Rocchio algorithm refines an initial query based on vector feedback:

𝑞(𝑜𝑝𝑡)=𝜇*𝑅+𝜇′*𝑅′−𝜇′′*𝑁𝑅

Where:
R is the centroid of relevant documents
R′ is the centroid of the most relevant documents
NR is the centroid of non-relevant documents

Cosine similarity is used to measure how close each document is to the query or to the optimized query.
If a document has a high cosine similarity, it means its direction in the vector space is close to that of the query.

By adjusting the query vector using Rocchio, we increase the importance of useful terms and suppress irrelevant ones.

📂 Project Structure
├── rocchio_algohrithm.ipynb      # Full notebook with all steps and views

🔧 How to Run the Project
1. Install Dependencies
pip install numpy pandas scikit-learn

2. Run the Notebook

Open:

rocchio.ipynb


And execute all cells.

3. Or Run the Python Script
python main.py

📊 What the Program Produces
✔ View 1 — TF-IDF Matrix + Cosine Similarities

A table showing all 50 documents, their tf-idf scores using the sports vocabulary, and their similarity to the initial query.

✔ View 2 — Top 20% Relevant Documents

Sorted by cosine similarity.

✔ View 3 — Bottom 80% Non-Relevant Documents

Used to compute NR.

✔ View 4 — Vector R

Average vector of relevant documents.

✔ View 5 — Vector R′

Average vector of the strongest relevant documents.

✔ View 6 — Vector NR

Average vector of non-relevant documents.

✔ View 7 — Optimized Query Vector q(opt).
	​

The final refined query produced by the Rocchio formula.

✔ View 8 — Top 5 Terms

The terms with the highest positive weight in the optimized query.

✔ View 9 — Top 3 Closest Documents

Documents with the highest cosine similarity to q(opt).


🎯 Key Concepts Demonstrated

Vector Space Model

Term Frequency–Inverse Document Frequency (tf-idf)

Cosine similarity

Relevance feedback

Query optimization

Centroid computation

Ranking documents by similarity

This project shows how vector-based text retrieval systems operate under the hood and how query refinement can significantly improve search performance.

📘 Why This Project Matters

Understanding Rocchio and similarity measures is important for:

Search engines

Recommendation systems

Information retrieval

Text mining

NLP vector representations

This project demonstrates the entire cycle clearly and with transparent intermediate results.
