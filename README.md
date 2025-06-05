
# 🎓 AI Career Guidance Chatbot (Hybrid ML + Gemini AI)

This is a web application built using **Streamlit**, **Scikit-learn**, and **Google Gemini Pro API** that acts as an AI-powered career counselor. It offers intelligent career advice by first classifying your interests into a career domain using a trained ML model and then generating personalized career suggestions using **Gemini AI**.

---

## 🔍 Features

- Lightweight interest classifier (Naive Bayes) trained on sample data
- Real-time career advice using Google Gemini Pro API
- Integrated ML + LLM workflow
- Easy deployment with Streamlit
- Secure API key management with `secrets.toml`

---

## 🚀 Demo

![Demo Screenshot](assets/demo_screenshot.png)  
*(Replace with actual screenshot after running)*

---

## 🧠 Technologies Used

- [Streamlit](https://streamlit.io/) – UI
- [Scikit-learn](https://scikit-learn.org/) – Text classification
- [Google Generative AI (Gemini)](https://ai.google.dev/) – Career recommendations
- Python 3.8+

---

## 📁 Project Structure

```bash
ai_career_chatbot_gemini/
├── ai_career_chatbot_gemini.py      # Main Streamlit app combining ML + Gemini AI
├── model_train.py                   # Script to train the Naive Bayes model
├── interest_model.pkl               # Saved trained ML model (TF-IDF + Naive Bayes)
├── career_interests.csv             # Sample labeled dataset (interests → domain)
├── requirements.txt                 # Required Python packages
├── README.md                        # Project documentation (this file)
├── assets/
│   └── demo_screenshot.png          # Screenshot(s) of UI and results
├── .streamlit/
│   └── secrets.toml                 # Gemini API key configuration
```

### 📌 Key Components:

- **`ai_career_chatbot_gemini.py`**: Streamlit app that handles user input, uses the ML model to classify career domain, then fetches recommendations using Gemini.
- **`model_train.py`**: Trains and saves the text classification model.
- **`interest_model.pkl`**: The serialized machine learning model used for domain classification.
- **`career_interests.csv`**: Dataset with interest texts and corresponding career domains (used for training).
- **`.streamlit/secrets.toml`**: Stores your Gemini API key securely.
- **`assets/`**: Folder for UI screenshots and visuals to showcase in the report or README.

---

## 🔐 Setup Secrets

Create a `.streamlit/secrets.toml` file with:

```toml
gemini_api_key = "your_actual_gemini_api_key"
```

---

## 🛠️ Installation & Running

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/ai_career_chatbot_gemini.git
cd ai_career_chatbot_gemini
```

2. **Install dependencies**:

```bash
pip install -r requirements.txt
```

3. **Run the app**:

```bash
streamlit run ai_career_chatbot_gemini.py
```

---

## 📦 requirements.txt

```text
streamlit
google-generativeai
scikit-learn
pandas
```

---

## ✨ How It Works

1. **User enters interests and strengths** (e.g., "I love coding and solving problems").
2. A **Naive Bayes model** classifies the input into a domain (e.g., Technology, Arts, Medicine).
3. The app prompts **Gemini Pro** to generate **2–3 career suggestions** in that domain.
4. Output is shown in a user-friendly interface.

---

## 🧑‍💼 Example

### ✅ Input:
> I enjoy chemistry and biology. I want to work in healthcare.

### 🧠 ML Classifier Output:
> **Predicted Domain:** Medicine

### 🤖 Gemini Career Suggestions:
1. Pharmacist  
2. Biotech Researcher  
3. Clinical Lab Technician

---

## 📊 Evaluation (ML Model)

Sample metrics (from test set):

- **Accuracy**: 92%  
- **F1 Score**: 0.93  
- **Algorithm**: Naive Bayes (TF-IDF + MultinomialNB)

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgements

- Google AI Studio  
- Streamlit Community  
- Scikit-learn Documentation  
