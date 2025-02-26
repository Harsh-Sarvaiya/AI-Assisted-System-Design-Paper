# AI-Assisted System Design: Improving Sequence Diagrams Through Use Case Scenarios

## 📌 Overview
This repository contains the implementation and research paper for **AI-Assisted System Design**, which explores the automation of generating **UML Sequence Diagrams** (SDs) from **User Stories (USs)** using OpenAI’s GPT-4 model.

The project evaluates two AI-driven pipelines:
- **Pipeline A**: Directly converts User Stories into Sequence Diagrams.
- **Pipeline B**: Introduces an intermediate step—Use Case Scenario (UCS) generation—before converting to Sequence Diagrams.

📄 **Read the full paper:** [IEEE Conference Paper](./IEEE_Conference_Template.pdf)

## 🚀 Features
- **Automated UML Sequence Diagram Generation**
- **Comparison of Direct vs. Intermediate Approach**
- **Integration with OpenAI’s GPT-4 for AI-assisted modeling**
- **Use of PlantUML for visual rendering**
- **Empirical evaluation of accuracy, relevance, and complexity**

## 📊 Key Findings
- **Pipeline B**, which introduces **Use Case Scenarios**, significantly enhances the quality and structure of generated Sequence Diagrams.
- AI-generated diagrams are **clearer, more detailed, and logically consistent** when an intermediate step is included.
- The study highlights how **AI can streamline software development**, reducing human effort while improving precision in requirement modeling.

## 🔧 Installation & Setup
To run the AI-driven Sequence Diagram generator, follow these steps:

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Harsh-Sarvaiya/AI-Assisted-System-Design.git
cd AI-Assisted-System-Design
```

### 2️⃣ Install Dependencies
This project runs on Python 3 and requires the following libraries:
```bash
pip install openai plantuml requests pandas python-docx python-dotenv
```

### 3️⃣ Set Up OpenAI API Key
You'll need an OpenAI API key to generate sequence diagrams:
```bash
export OPENAI_API_KEY="your-api-key-here"
```
Or use a `.env` file:
```python
from dotenv import load_dotenv
load_dotenv()
openai.api_key = os.getenv("OPENAI_API_KEY")
```

## 🔄 Usage

### Generate a Sequence Diagram (Pipeline A - Direct Approach)
```bash
python pipeline_A.py --input user_stories.csv
```

### Generate a Sequence Diagram (Pipeline B - Use Case Scenario Approach)
```bash
python pipeline_B.py --input user_stories.csv
```

### View Generated UML Diagrams
All diagrams will be saved as `.puml` and rendered as `.png` in the `plantuml_sequences/` directory.

## 📚 Dataset
The user stories dataset is sourced from **Jahan et al. (2023)** and includes real-world software development requirements from **library and restaurant management systems**.

## 📈 Results
| Approach | Accuracy | Relevance | Complexity |
|----------|---------|---------|------------|
| **Pipeline A** | 9.0 | 9.0 | 0.46 |
| **Pipeline B** | 9.4 | 9.6 | 1.0 |

**Evaluator Agreement:**
Pearson Correlation: **0.99** | Spearman: **0.73** | Kendall: **0.57**

📌 The introduction of Use Case Scenarios in **Pipeline B** improved clarity and logical consistency of the final diagrams.

## 📜 Citation
If you use this work in your research, please cite:
```
@inproceedings{sarvaiya2024ai,
  author    = {Harsh Sarvaiya, Munima Jahan},
  title     = {AI-Assisted System Design: Improving Sequence Diagrams Through Use Case Scenarios},
  year      = {2025},
}
```

## 🤝 Contributors
- **Harsh Sarvaiya** ([LinkedIn](https://www.linkedin.com/in/harsh-sarvaiya/))
- **Dr. Munima Jahan**

## 📬 Contact
For questions, reach out via:
📧 Email: hsarvaiya.work@gmail.com


---
⭐ If you find this useful, consider starring this repo!
