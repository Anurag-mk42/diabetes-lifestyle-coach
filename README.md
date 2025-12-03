# Diabetes Lifestyle Coach - Multi-Agent AI

An intelligent health companion agent for tracking diabetes lifestyle metrics and providing educational guidance based on transparent, rule-based analysis.

## Overview

This project implements a **multi-agent artificial intelligence system** that helps people with diabetes:
- Track daily fasting blood sugar readings
- Monitor physical activity (steps)
- Log food intake and dietary notes
- Receive instant feedback on health metrics
- Get personalized lifestyle recommendations
- Prepare informed questions for doctor visits

## Features

✅ **Daily Health Logging**
- Log fasting blood sugar (mg/dL)
- Record daily steps walked
- Note meals and food intake
- Immediate color-coded feedback (GREEN/YELLOW/RED)

✅ **Weekly Analysis & Trends**
- View 7-day health summaries
- Track average blood sugar levels
- Monitor activity achievements vs. daily goals
- Identify concerning patterns

✅ **Rule-Based Medical Flagging**
- Transparent, explainable analysis using public health guidelines
- No black-box AI - all logic is clear and transparent
- Flags concerning patterns (elevated sugar, low activity)
- Generates urgency alerts for dangerous readings

✅ **Personalized Recommendations**
- Suggests post-meal walks
- Recommends activity adjustments
- Provides nutrition guidance
- Generates doctor visit questions

✅ **Educational Disclaimers**
- Clear medical disclaimers on all interactions
- Emphasizes consulting healthcare providers
- Uses public health ranges (individual targets vary)

## Health Ranges (Educational References)

These are based on public health guidelines. **Your personal targets may differ** - always follow your doctor's advice.

**Fasting Blood Sugar (mg/dL):**
- **Below 70**: LOW - Risk of hypoglycemia, watch for symptoms
- **80-130**: NORMAL - Common target range for many people
- **131-180**: ELEVATED - Lifestyle changes recommended
- **Above 180**: HIGH - Medical review strongly recommended

**Activity:**
- Goal: 7,000-10,000 steps daily (adjustable)
- Post-meal walks (10-15 mins) help control blood sugar

## How to Use

### Option 1: Kaggle Notebook (Recommended)
1. Visit the [Kaggle Notebook](https://www.kaggle.com/code/alephs0/notebook9ff98dd6b9)
2. Click "Copy & Edit"
3. Run the code cells
4. Interact with the system

### Option 2: Local Python
```bash
git clone https://github.com/Anurag-mk42/diabetes-lifestyle-coach.git
cd diabetes-lifestyle-coach
python diabetes_coach.py
```

### Example Workflow
```python
# Initialize
health_log = HealthLog()

# Log today's data
health_log.log_entry('2025-12-03', 145, 5200, 'rice, curry, chai')

# Get 7-day summary
history = health_log.get_history(7)
print(f"Avg Sugar: {history['avg_sugar']} mg/dL")

# Get analysis with recommendations
analysis = health_log.analyze(7)
for flag in analysis['flags']:
    print(flag)
```

## Architecture

**Multi-Agent Components:**
1. **IntakeAgent**: Collects daily health measurements
2. **AnalysisAgent**: Applies rule-based analysis and flagging
3. **CoachAgent**: Generates personalized recommendations
4. **CoordinatorAgent**: Orchestrates multi-agent workflow

**Tools:**
- `log_entry()`: Record daily measurements
- `get_history()`: Retrieve and summarize health data
- `analyze()`: Analyze patterns and flag concerns
- `lifestyle_plan()`: Generate weekly recommendations

**Key Features:**
- In-memory session management
- Persistent health log storage
- Transparent rule-based logic
- Context engineering for efficiency

## Disclaimer

⚠️ **IMPORTANT**: This is an **educational tool only**. It is **NOT** a medical device or medical advice system.

- This system does NOT diagnose diabetes or any medical condition
- Blood sugar ranges shown are **educational references** based on public health guidelines
- **Your personal targets must be set by YOUR healthcare provider**
- Always consult with your doctor or healthcare provider before making any health decisions
- In case of medical emergencies, seek immediate professional medical help
- This tool helps organize data and prepare for doctor visits - it does not replace medical care

## Technical Details

**Built With:**
- Python 3.8+
- Gemini API (optional, for LLM-powered enhancements)
- Kaggle Notebook runtime

**Demonstrates:**
- Multi-agent AI architecture
- Tool-based agent systems
- Session and memory management
- Rule-based reasoning
- Educational health technology

## For Kaggle Capstone Submission

**Track:** Agents for Good (Healthcare)

**Submission Link:** [Kaggle Notebook - Diabetes Lifestyle Coach](https://www.kaggle.com/code/alephs0/notebook9ff98dd6b9)

**Problem Solved:** Helps people with diabetes organize health data, identify patterns, and prepare informed conversations with healthcare providers.

## File Structure
```
diabetes-lifestyle-coach/
├── README.md (this file)
├── diabetes_coach.py (main implementation)
├── notebook.ipynb (Kaggle notebook version)
└── requirements.txt (dependencies)
```

## Getting Help

- **Medical Questions**: Contact your healthcare provider
- **Technical Issues**: Open an issue on GitHub
- **Feature Requests**: Submit a pull request

## License

MIT License - Feel free to use, modify, and distribute

## Author

**Anurag Sarkar** - Kaggle Capstone Project 2025

---

**Remember**: Take care of your health! This tool helps you track and understand your lifestyle metrics, but medical decisions should always be made with your healthcare provider. 🏥
