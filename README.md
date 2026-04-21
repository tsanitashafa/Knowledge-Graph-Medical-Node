# Knowledge Graph Medical Node: Integrasi Wikidata & DBpedia Indonesia

Repository ini berisi proyek integrasi data *Knowledge Base* (Wikidata dan DBpedia Indonesia) serta analisis graf untuk memenuhi tugas mata kuliah Graf Pengetahuan.

## 👥 Tim Proyek
| Nama | NRP |
| :--- | :--- |
| **Ayu Alfia Putri** | 5026231033 |
| **Tsanita Shafa Hadinanda** | 5026231088 |

---

## 🛠️ Langkah-langkah Integrasi Data

### 1. Pengambilan Data (SPARQL Extraction)
Data diekstraksi dari dua sumber menggunakan kueri SPARQL:
* **Wikidata:** Mengambil daftar entitas medis utama.
* **DBpedia Indonesia:** Mengambil properti tambahan yang relevan melalui pencocokan label/string.

### 2. Penggabungan Data (Data Joining)
Data digabungkan menggunakan pustaka **Pandas** di Python. Proses integrasi ini memastikan data dari kedua sumber saling melengkapi berdasarkan kunci (ID/Label) yang sama.
* **Notebook Utama:** `UTS_GRAF.ipynb`
* **Data Sumber:** Folder `/data`

---

# Visualisasi Skema Graf (Ontologi)
Berikut adalah gambaran skema hubungan antar entitas (Node) dan relasi (Edge) yang terbentuk setelah proses integrasi:
<img width="412" height="434" alt="visualisation" src="https://github.com/user-attachments/assets/c7062622-4a80-4de9-8c66-950649ee6595" />

---

## 📊 Analisis Graf (Network Analysis)
Proyek ini merepresentasikan data medis sebagai graf (Node dan Edge) dan menerapkan analisis algoritma graf menggunakan **Neo4j** (berdasarkan file kueri Cypher).

* **Query Cypher:** `Query_Cypher.csv`
* **Algoritma yang Diterapkan:** Betweenness Centrality, Jaccard Similarity, Louvain Community

---

## 📂 Struktur Repositori
```text
.
├── data/               # Folder berisi dataset awal (CSV)
├── Query_Cypher.csv    # Kueri Cypher untuk implementasi di Neo4j
├── README.md           # Dokumentasi proyek
└── UTS_GRAF.ipynb      # Notebook proses integrasi & analisis graf
