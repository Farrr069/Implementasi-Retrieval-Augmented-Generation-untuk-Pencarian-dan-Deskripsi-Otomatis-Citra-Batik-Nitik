Implementasi Retrieval-Augmented Generation untuk Pencarian dan Deskripsi Otomatis Citra Batik Nitik

Proyek ini mengembangkan sistem Retrieval-Augmented Generation (RAG) berbasis citra untuk mengeksplorasi kekayaan budaya Indonesia melalui motif Batik Nitik. Sistem mengintegrasikan teknologi pencarian berbasis vector similarity menggunakan CLIP dan FAISS, serta pembuatan deskripsi generatif otomatis melalui model BLIP, dengan opsi perluasan menggunakan GPT-4 atau Stable Diffusion.

📌 Tujuan

Menyediakan platform interaktif berbasis AI yang memungkinkan pengguna:

Menginput teks atau gambar sebagai query

Menemukan gambar batik Nitik yang relevan

Menerima deskripsi otomatis terkait filosofi, motif, atau makna visual batik

(Opsional) Menghasilkan variasi baru dari motif yang ada

🖼️ Dataset

Dataset yang digunakan adalah Batik Nitik 960, terdiri dari 960 gambar batik dengan metadata naratif dwibahasa (Indonesia & Inggris) yang menjelaskan motif, filosofi, dan nama batik. Data telah diproses dan diaugmentasi (rotasi 90°, 180°, 270°) untuk memperkaya variasi dan memperkuat kemampuan generalisasi sistem.

🔗 Download Dataset:
[Batik Nitik 960 on Mendeley Data](https://data.mendeley.com/datasets/sgh484jxzy/3)

🧠 Arsitektur Sistem
🔍 Image Retrieval

Input: Teks deskripsi atau gambar batik

Encoder: CLIP (ViT-B/32)

Indexing: FAISS (cosine similarity)

Output: Top-k gambar batik paling relevan

📝 Generatif

Captioning: BLIP untuk deskripsi otomatis naratif

Generasi gambar (opsional): Stable Diffusion / SDXL

Prompt builder: Berdasarkan metadata + hasil retrieval

💡 Alur Pipeline
[Input: Teks/Gambar] → CLIP Encoder → FAISS Search → Top-k Image → BLIP → Narasi Otomatis
                                                                 ↓
                                                       (opsional) Stable Diffusion → Gambar Baru

🔬 Evaluasi

Retrieval: Top-k Accuracy, Precision@k, MRR, Cosine Similarity

Generatif Teks: BLEU Score, CLIP Similarity, Penilaian Manual

Generatif Gambar (opsional): FID Score, CLIP Score, Human Assessment

🖥️ Teknologi yang Digunakan

Python, PyTorch, Jupyter Notebook

CLIP (OpenAI)

BLIP (Salesforce)

FAISS (Facebook AI)

Streamlit atau Gradio untuk UI

👥 Tim

Ahmad Safandi – Data Engineer & Preprocessing

Farrel Maulana Irfan – Image Retrieval Developer

Mohamad Mujahidin – 

Aji Alfrian – UI/UX Developer & Integrator

📆 Timeline

Minggu 1: Preprocessing + Image Retrieval

Minggu 2: Generatif + UI Development

Minggu 3: Integrasi, Evaluasi, Dokumentasi & Demo

🙏 Acknowledgment

Proyek ini merupakan bagian dari tugas akhir program sarjana di Departemen Informatika, Universitas Muhammadiyah Malang. Sistem ini dikembangkan menggunakan framework open-source: CLIP, BLIP, dan FAISS. Terima kasih kepada para dosen pembimbing atas bimbingan dan fasilitas komputasi yang telah diberikan.
