<div align="center">
  
# 🩺 MedLog

<p align="center">
  <img src="MedLog.png" alt="Med|Log Logo" style="max-width: 100%; height: auto; >
</p>
    
---

**An Expert System for Medical Diagnosis, Emergency Detection, and Lifestyle Advice**

MedLog is a rule-based expert system written in **SWI-Prolog**. It models a small medical knowledge base of patients, symptoms, and diseases, then uses logical inference to diagnose conditions, flag emergencies, suggest treatments, and offer lifestyle and preventive advice.

</div>

---

## ✨ Features

- **Symptom-based diagnosis** — infers diseases (flu, COVID-19, hypertension, diabetes, dengue) from a patient's recorded symptoms.
- **Emergency detection** — raises an alert when critical symptoms (chest pain, difficulty breathing, unconsciousness) occur together.
- **Treatment suggestions** — maps each diagnosed disease to recommended care.
- **Lifestyle advice** — provides tailored, condition-specific guidance.
- **Preventive measures** — lists ways to reduce the risk of each disease.
- **Symptom severity tracking** — classifies symptoms as *mild*, *moderate*, *high*, or *critical*.
- **Hospital referral system** — recommends ICU, specialist consultation, or home care based on condition.
- **Multi-disease diagnosis** — collects all possible diseases for a patient using `findall/3`.
- **Risk factor & allergy records** — stores per-patient risk factors and known allergies.

---

## 📂 Repository Structure

| File | Description |
|------|-------------|
| `MedLog SWI-Prolog.pl` | The Prolog knowledge base and inference rules |
| `MedLog Knowledge Base Diagram.png` | Visual overview of the knowledge base |
| `MedLog.pdf` | Project documentation / report |
| `LICENSE` | Apache-2.0 license |

---

## 🚀 Getting Started

### Prerequisites

Install [SWI-Prolog](https://www.swi-prolog.org/download/stable).

### Run

```bash
swipl "MedLog SWI-Prolog.pl"
```

---

## 💡 Example Queries

Once the knowledge base is loaded, try:

```prolog
% Diagnose a specific patient
?- has_disease(mukit, Disease).
Disease = flu.

% Check for a medical emergency
?- emergency(sadman).
true.

% Get a treatment recommendation
?- has_disease(rakib, D), treatment(D, Advice).
D = covid19,
Advice = 'Isolate, monitor oxygen level, consult a doctor'.

% Lifestyle advice for a patient
?- lifestyle_advice(nirob, Advice).
Advice = 'Exercise daily and maintain a low-sodium diet'.

% Hospital referral decision
?- refer_hospital(lamia, Recommendation).
Recommendation = 'Specialist Consultation Needed'.

% List all possible diseases for a patient
?- possible_diseases(rakib, Diseases).
Diseases = [covid19].
```

---

## 🧠 How It Works

MedLog stores clinical knowledge as Prolog **facts** (symptoms, risk factors, allergies, severities) and **rules** (diagnosis, emergency, referral, advice). When you pose a query, Prolog's inference engine unifies the query against these rules and backtracks to find every valid answer — the essence of an expert system.

---

## ⚠️ Disclaimer

MedLog is an **academic / educational project** demonstrating expert systems and logic programming. It is **not** a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider.

---

## 📜 License

This project is licensed under the **Apache-2.0 License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**[bokhtearmdabid](https://github.com/bokhtearmdabid)**
