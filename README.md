# Multimodal Hate Speech Detection in Dravidian Languages  
### Team ML_Forge @ DravidianLangTech 2025  

📄 **Paper:** https://aclanthology.org/2025.dravidianlangtech-1.68/  
📑 **PDF:** https://aclanthology.org/2025.dravidianlangtech-1.68.pdf  

---

## 🔍 Overview  

Hate speech detection in Dravidian languages—**Malayalam, Tamil & Telugu**—is challenging due to:

- Complex grammar and linguistic richness  
- Dialect variation  
- Code-mixing with English  
- Rise of multimodal (text + audio) content  

This repository contains our **official submission** to the  
**Multimodal Hate Speech Detection** shared task at  
**DravidianLangTech@NAACL 2025**.

We experimented with **mBERT, T5** for text and **Wav2Vec2, Whisper** for audio.  
Overall, **mBERT + Wav2Vec2** provided the best performance.

---

## 🧠 Task Description  

Dataset includes YouTube-sourced content labeled into:

| Label | Meaning |
|-------|---------|
| **G** | Gender-based Hate |
| **P** | Political Hate |
| **R** | Religious Hate |
| **C** | Personal Defamation |
| **NH** | Non-Hate |

Each sample includes **Text + Raw Audio**, enabling multimodal classification.

---

## 🚀 Our Approach  

### 🔤 **Text Models Utilized**
- **mBERT** — Best performing text encoder  
- **T5 Base** — Underperformed compared to mBERT  

### 🔊 **Audio Models Utilized**
- **Wav2Vec2 (Self-Supervised)** — Final chosen audio model  
- **Whisper Base** — Higher resource cost, lower F1 in our setup  

### 🛠️ Technical Pipeline  
1. Text preprocessing (punctuation cleanup, normalization, language ID handling)  
2. Audio feature extraction using **Wav2Vec2**  
3. Fine-tuning models for 5-way classification  
4. Combining predictions via simple ensemble  

---

## ⭐ Acknowledgements

We thank the DravidianLangTech 2025 Organizing Committee for dataset access and task support.

## 📌 License

This project follows the licensing rules of:
1. DravidianLangTech 2025 Shared Task Dataset
2. HuggingFace models used (mBERT, T5, Wav2Vec2, Whisper)
Check individual licenses before commercial use.


## 📖 Citation
If you use this work in your research, please cite the following paper:

```bibtex
@inproceedings{faisal2025mlforge,
  title={Team ML_Forge@DravidianLangTech 2025: Multimodal Hate Speech Detection in Dravidian Languages},
  author={Adnan Faisal and Shiti Chowdhury and Sajib Bhattacharjee and Udoy Das and Samia Rahman and Momtazul Arefin Labib and Hasan Murad},
  booktitle={Proceedings of the Fifth Workshop on Speech, Vision, and Language Technologies for Dravidian Languages},
  pages={381--386},
  year={2025},
  address={Acoma, Albuquerque Convention Center, New Mexico},
  publisher={Association for Computational Linguistics},
  doi={10.18653/v1/2025.dravidianlangtech-1.68}
}

---
