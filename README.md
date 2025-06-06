# ChartMind: Interpretable Reasoning from Chart Images using Large Language Models

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1N-Mhll1_G9GYHZnlrRON4LRRcaA_f9Da)

**ChartMind** is an AI-powered Jupyter Notebook project that demonstrates how multimodal large language models (LLMs), like Google’s Gemini Vision, can generate interpretable reasoning from data visualizations. Given any chart image—such as bar charts, line plots, radial maps, or scatter plots—ChartMind can:

- Generate multiple-choice questions (MCQs)
- Provide step-by-step Chain-of-Thought (CoT) reasoning
- Visualize the reasoning as an annotated flowchart

The goal is to make LLM reasoning **visible, understandable, and educational** for analysts, students, and decision-makers engaging with visual data.

> While this implementation uses **COVID-19 charts as examples**, the pipeline is designed to work with **any chart image** from any domain.

---

## What ChartMind Does

- Accepts a chart image (e.g., `.png`, `.jpg`)
- Uses Gemini Vision to:
  - Describe the chart
  - Generate 2 multiple-choice questions (MCQs)
  - Generate reasoning using Chain-of-Thought (CoT) explanations
- Visualizes the reasoning flow using **Graphviz**
- Provides interpretability dashboards and evaluation metrics across multiple charts

---

## Technologies Used

- **Python** (Jupyter Notebook)
- **Google Gemini Vision API** (via `google-generativeai`)
- NLP: `transformers`, `sentence-transformers`
- Visualization: `graphviz`, `matplotlib`, `wordcloud`, `seaborn`
- Analysis: `scikit-learn`, `pandas`, `numpy`

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/chartmind.git
cd chartmind
````

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Your API Key

Create a `.env` file in the root folder:

```
GEMINI_API_KEY=your_api_key_here
```

Alternatively, the notebook will prompt for manual input if needed.

---

## Example Workflow

1. Upload any chart image.
2. Gemini generates a title + 2 MCQs.
3. CoT reasoning is extracted per question.
4. Flowchart is rendered showing reasoning steps.
5. Additional cells analyze reasoning quality using:

   * Heatmaps
   * Radar plots
   * PCA clustering
   * Word clouds

---

## Example Use Cases

Although this demo uses charts related to **pandemic case trends and vaccination patterns**, ChartMind can be applied to:

* Economic indicators
* Sports analytics
* Marketing dashboards
* Climate change charts
* Academic or research visualizations

> If a human can interpret the chart, ChartMind aims to show how an AI might reason through it.

---

## Evaluation & Insights

The notebook also includes cells to analyze and compare reasoning quality:

* Cognitive Feature Heatmap – Measures traits like "mentions axis", "confidence boost", "label usage"
* Radar Plots – Compare reasoning spread across visualizations
* Nebula Charts – Visualize reasoning structure similarity
* PCA Clustering – Analyze semantic summary complexity
* Word Cloud – Extracts frequently used reasoning terms

These help assess the interpretability, fluency, and structure of LLM-generated reasoning.

---

## Author

**Dushyant Singh Pawar**
M.S. in Computer Science — UNC Charlotte | [dpawar4@charlotte.edu](mailto:dpawar4@charlotte.edu) | [LinkedIn](https://www.linkedin.com/in/dushyantsinghpawar/) • [GitHub](https://github.com/dushyantsinghpawar)

---

## License

This project is licensed under the MIT License.
You're welcome to use, adapt, and extend it with attribution.

---

## Feedback & Contributions

If you find this project useful or want to collaborate on building interpretable AI tools for visual analytics, feel free to open an issue or connect on LinkedIn.

> Star this repo if you'd like to support future extensions (like a Streamlit or Gradio version)!
