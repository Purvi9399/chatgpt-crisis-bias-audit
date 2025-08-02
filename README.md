# chatgpt-crisis-bias-audit

# 🧠 ChatGPT in Crisis: Can Language Models Understand Distress?

This project investigates how large language models (LLMs), particularly ChatGPT , respond to emotionally distressing prompts, especially when those prompts include markers of identity such as race, gender, or culture. As LLMs are increasingly deployed in sensitive domains like mental health, customer support, and social platforms, it is critical to ask: **Can these models truly understand distress? And do they respond equitably across different identities?**

---

## 🎯 Project Goal

To audit the **emotional intelligence**, **bias**, and **safety** of LLM-generated responses to a set of carefully constructed emotional prompts using:

- Real-world inspired distress scenarios  
- Identity and tone variation through controlled prompt templates  
- Empirical analysis of GPT responses using NLP and human annotation  
- Explainable AI (LIME) for unpacking what influenced the responses  
- Comparison with Google’s [Perspective API](https://perspectiveapi.com/) on toxicity, empathy, and stability  

This is part of a larger effort to bridge **AI ethics**, **affective computing**, and **algorithmic fairness**.

---

## 📁 Project Structure

<pre> chatgpt-crisis-bias-audit/ 
├── data/ │
├── prompts.csv # Crafted emotional prompts (100–200) │ 
├── gpt_responses.csv #GPT outputs with metadata 
 └── annotations.csv #Human empathy/safety ratings 
├── analysis/ 
│ └── response_analysis.ipynb # Sentiment, LIME, bias visualisation 
├── ethics/ │ 
├── ethics_memo.md # Ethical reflections on harms & use 
│ └── related_research.md # Annotated academic references
├── app/ 
│ └── streamlit_app.py # Optional Streamlit visualisation tool 
├── README.md 
├── requirements.txt 
└── LICENSE </pre>


---

## 🧪 Methodology

### 1. **Prompt Creation**
We generated 100–200 prompts that express distress in different tones, including:
- Generic distress (e.g., “I don’t feel okay today”)
- Identity-tagged (e.g., “As a gay teen, I feel invisible”)
- Emotional nuance (e.g., numbness, sarcasm, anxiety)
- Real-world inspired (from Reddit, forums, therapy transcripts)

### 2. **Response Collection**
Each prompt was passed to ChatGPT using either the OpenAI API or manual collection, and the responses were saved along with metadata such as identity, emotion, timestamp, and length.

### 3. **Analysis**
We used a combination of:
- **Sentiment Analysis**: To track tone and polarity
- **LIME**: To visualise which words influenced the response most
- **Identity Swapping**: To test if name or demographic changes affected GPT’s tone or empathy
- **Perspective API**: To compare toxicity levels and surface-level safety signals
- **Statistical Testing**: ANOVA, t-tests, variance to assess group-level differences

---

## 🔍 Key Findings (Work in Progress)

- ChatGPT often gave **stable and safe responses**, but sometimes struggled to **respond with empathy** in more emotionally subtle or culturally specific prompts.
- In some cases, **changing identity markers** (e.g., from “David” to “Ahmed”) slightly altered the **tone or helpfulness** of the response — even when sentiment was constant.
- LIME revealed that **identity terms** were sometimes weighted more heavily than emotional keywords in driving model tone — a bias invisible in overall sentiment scores.
- Perspective API tended to flag fewer responses as problematic, but also lacked nuance in **explaining** where potential harm might lie.

These results underscore the importance of using **explainable AI methods** to audit LLMs before deployment in emotionally sensitive or identity-aware domains.

---

## 🛠 Tech Stack

- Python (pandas, matplotlib, scikit-learn)
- OpenAI GPT-3.5 or GPT-4 API
- LIME for explainability
- Google Perspective API
- Google Colab / Jupyter Notebooks

---

## ✍️ Author & Vision

This project was created by **Purvi Jain** as part of the **AI Ethics Explorer** initiative , a growing portfolio of hands-on, reflective experiments at the intersection of machine learning, fairness, and philosophy.

🔗 [https://purvi9399.github.io](https://purvi9399.github.io)

---

## 📚 References & Inspiration

- Binns et al. (2018). “’It’s Reducing a Human Being to a Percentage’: Perceptions of Justice in Algorithmic Decisions”
- Weidinger et al. (2021). “Ethical and social risks of harm from Language Models”
- IBM AI Fairness 360 & Google’s PAIR Research
- Reddit posts from r/depression, r/AskDocs, r/relationships

---

## 🧠 License & Reuse

Open-sourced for research and educational use under the MIT License.  
Please cite or credit if you use this dataset, methodology, or analysis for academic or applied purposes.
