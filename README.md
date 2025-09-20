# InsightMate: AI-Assisted Persona Generation

**What it is:**  
InsightMate is a human-centred AI tool that transforms behavioural data into explainable, marketer-friendly personas.  
It combines K-Means clustering with LLM-based narrative formatting and is paired with a clickable Figma prototype for end-to-end demonstration.  

**Why this Project:**  
Traditional personas are often vague or stereotype-driven. InsightMate solves this by:  
- Clustering real behavioural data into clear audience segments  
- Explaining “why” traits appear with confidence scores and lineage  
- Formatting clusters into usable, narrative-style personas  
- Providing a transparent, interactive design prototype to explore insights  

---

## Demo
- **Project Report:** See 'doc/Report/InsightMate.pdf'
- **Video Walkthrough (90s):**   
- **Clickable Figma Prototype:** (https://www.figma.com/design/lLSsI6fuMtslfSNo7Y5nj3/InsightMate?node-id=0-1&t=Jdpojx7IrYEq6HTT-1)  
- **Screenshots:** See `docs/InsightMate_UI_Screenshots`  

---

## How it works (Backend)
1. **Input:** Synthetic dataset (`/data/sample_synthetic.csv`)  
2. **Preprocess:** Clean, scale, and encode features  
3. **Cluster:** Apply K-Means (k chosen with elbow/silhouette method)  
4. **Summarise:** Extract dominant traits per cluster  
5. **Format:** Convert traits into human-readable personas (LLM integration optional)  

Full pipeline in `InsightMate_Backend/InsightMate.ipynb`  

---

## How it works (Design)
- User uploads data → system clusters behaviours → personas generated  
- Personas can be compared, refined, or explored via behavioural timelines  
- Transparency features: tooltips, “How was this built?” modals, editable traits  
- Prototype built in Figma, mapping backend outputs to UI flows  

---

## Architecture
	•	Ingest → Preprocess → Cluster → Summarise → Persona Formatting → Export → UI
---

## Implemented
	•	K-Means clustering & persona generation pipeline
	•	Figma prototype demonstrating UI and flows
	•	Transparency features: tooltips, summary cards, confidence levels
	•	Poster, client presentation, and final report included
---

## Roadmap
	•	Lightweight Streamlit demo for live persona previews
	•	Evaluation metrics dashboard (silhouette scores, prompt evaluation)
	•	RAG Smart Mode for real-time external data integration
	•	Analyst Mode with weighting controls for advanced users
---

## Privacy
	•	No real user data included.
	•	All datasets are synthetic/mock for demonstration purposes.
---

## Hiring Note

I’m seeking a sponsored role in Data-Driven Design / AI UX.
InsightMate demonstrates my end-to-end capability: research → ML pipeline → UX design.
Let’s connect: oreoluwakushimo@gmail.com • LinkedIn: https://www.linkedin.com/in/oreoluwakushimo/


## Quickstart
```bash
# 1) Setup environment
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 2) Run the notebook
jupyter lab
# Open notebooks/InsightMate.ipynb and Run All

## Repo Structure

InsightMate/
├─ README.md
├─ LICENSE
├─ requirements.txt
├─ .gitignore
├─ data/
│   └─ shopping_behavior_updated.csv
├─ notebooks/
│   └─ InsightMate.ipynb
├─ docs/
│   ├─ InsightMate_Poster.pdf
│   └─ InsightMate_UI_Screenshots/
└─ demo/
    └─ demo.mp4
