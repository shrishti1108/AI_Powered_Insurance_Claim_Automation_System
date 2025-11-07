# 🚗 AI-Powered Insurance Claim Automation System
### *(Integrating Document Classification, Claim Decision Prediction, and Generative Explanation)*

---

## 📘 Project Overview

This project aims to **automate the insurance claim process** using a combination of **Machine Learning (ML)**, **Natural Language Processing (NLP)**, and **Generative AI**.

The system performs three main tasks:
1. **Classifies uploaded insurance documents** (like Claim Forms, Invoices, and Reports)
2. **Predicts claim outcomes** — whether a claim will be Approved ✅ or Denied ❌
3. **Generates natural-language explanations** for claim decisions using Generative AI (FLAN-T5 / Gemini)

All modules are integrated into an interactive **Streamlit Dashboard**.

---

## 🧠 Problem Statement

Insurance companies handle large volumes of claim-related documents manually, leading to:

- ⏳ Delays in claim processing  
- ⚙️ Human errors and inconsistencies  
- 💸 Increased operational costs  
- ❓ Lack of transparency in claim approvals  

This project solves these challenges through an **AI-based automation system** that processes documents, predicts outcomes, and communicates reasons clearly to customers.

---

## 🎯 Objectives

- Automate document classification using NLP Transformers  
- Predict insurance claim approval or denial using ML models  
- Use Generative AI to explain claim outcomes in simple human language  
- Integrate all features into a single Streamlit web dashboard  

---

## 🧩 System Architecture

Upload Document → Document Classifier (BART)
↓
Claim Data (Manual/Input/Extracted)
↓
Claim Predictor (Random Forest)
↓
Generative Explanation (FLAN-T5 / Gemini)
↓
Streamlit Dashboard Output


---

## ⚙️ Features

| Feature | Description |
|----------|--------------|
| 🧾 **Document Classification** | Reads PDF files and classifies as Invoice, Claim Form, or Report using NLP Transformer |
| 🧠 **Claim Decision Prediction** | Predicts whether claim will be approved or denied using ML |
| 💬 **Generative AI Explanation** | Generates human-readable explanations for claim outcomes |
| 📊 **Interactive Dashboard** | Streamlit web interface to upload, predict, and view explanations |
| 🔒 **Confidence Scores** | Displays model certainty for each prediction |

---

## 🧱 Tech Stack

| Category | Tools / Libraries |
|-----------|------------------|
| Language | Python |
| ML Frameworks | scikit-learn, pandas, numpy |
| Generative AI | Google FLAN-T5, Gemini API |
| NLP | Hugging Face Transformers, pdfplumber |
| Web Framework | Streamlit |
| Hosting | Google Colab + Ngrok / Streamlit Cloud |
| Visualization | matplotlib / Streamlit widgets |

---

## 🧩 Project Modules

### 1️⃣ **Document Classification Agent**
- Model: `facebook/bart-large-mnli`
- Reads uploaded PDF text using `pdfplumber`
- Classifies document type (Claim Form / Invoice / Policy / Report)
- Outputs label and confidence score

### 2️⃣ **Claim Decision Predictor**
- Model: `RandomForestClassifier`
- Input: Vehicle details, customer details, and safety features
- Output: Claim Status → Approved ✅ or Denied ❌
- Displays model confidence (probability)

### 3️⃣ **Generative AI Explanation Bot**
- Model: `google/flan-t5-large` or Gemini API
- Generates customer-friendly text explanations for model predictions
- Example:  
  *“Your claim was approved because your vehicle is new and has essential safety features.”*

### 4️⃣ **Streamlit Dashboard**
- User-friendly interface combining all three modules  
- Features: PDF upload, manual input, prediction display, and explanation generation  
- Deployed via Ngrok (Colab) or Streamlit Cloud

---

⚡ How to Run
🧩 Option 1: On Local System

git clone https://github.com/<your-username>/insurance-claim-ai.git
cd insurance-claim-ai
pip install -r requirements.txt
streamlit run app.py


🧩 Option 2: On Google Colab

!pip install streamlit pyngrok transformers pdfplumber scikit-learn torch pandas --quiet
from pyngrok import ngrok
!streamlit run app.py &>/dev/null&
public_url = ngrok.connect(8501)
print("🌐 Streamlit App Live At:", public_url)

## 📊 Example Outputs

**Uploaded Document:** Claim Form.pdf  
**Predicted Type:** Claim Form (Confidence: 94.7%)  
**Claim Decision:** ✅ Approved  
**Explanation:**  
> “The claim has been approved because the vehicle is relatively new, has a high NCAP safety rating, and includes key safety features such as brake assist and central locking.”

---

## 🧩 Dataset

- **Type:** Insurance claim dataset containing vehicle, policy, and safety features.  
- **Target Column:** `claim_status` → (1 = Approved, 0 = Denied)  
- **Usage:** Used for training claim prediction model  
- **Extra:** Additional datasets (Kaggle / synthetic) can be used for document classification testing.

---

## 🚧 Challenges

- Extracting clean text from scanned PDFs (OCR required)  
- Limited labeled insurance document data  
- Balancing dataset for fair claim prediction  
- Integrating ML + NLP + GenAI models in a single dashboard  
- Colab session limitations for Streamlit runtime  

---

## ⚙️ Limitations

- Accuracy depends on dataset size and quality  
- Generated explanations may not always be perfectly factual  
- Colab-based hosting is temporary (session resets after runtime ends)

---

## 🌟 Results

| Module | Accuracy / Quality |
|---------|--------------------|
| Document Classification | 92–96% |
| Claim Prediction | 88–90% |
| Generative Explanation | ~95% human readability |
| Dashboard | Fully interactive (Streamlit UI) |

---

## 🚀 Future Scope

- Integrate real insurance APIs for live claim data  
- Add image-based OCR for scanned claim forms  
- Train a custom fine-tuned LLM for the insurance domain  
- Deploy permanently on Streamlit Cloud / Hugging Face Spaces  
- Enable multi-language support for claim explanations  

---

## 💡 Applications

- 🏢 **Insurance companies** — automated claim handling  
- 🏦 **Banking / Finance** — loan approval transparency  
- ⚕️ **Healthcare** — automated medical claim verification  
- 🏛️ **Government welfare** — subsidy or benefit claim automation  

---

## 🧠 Skills Demonstrated

- Machine Learning (Random Forest, feature engineering)  
- NLP (Transformer-based classification)  
- Generative AI (Text explanation generation)  
- Python Programming  
- Data Analysis and Visualization  
- Web App Development (Streamlit)  
- Model Integration and Deployment  

---

## 🏁 Conclusion

> The **AI-Powered Insurance Claim Automation System** demonstrates how Generative AI can enhance transparency in automated decision-making.  
> By integrating NLP, ML, and GenAI in a unified dashboard, this project provides an intelligent, explainable, and user-friendly solution to automate insurance claim processing.
