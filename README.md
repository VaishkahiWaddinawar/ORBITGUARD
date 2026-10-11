ORBITGUARD – AI-Assisted Space Debris Risk Prediction

**Team Name:* CORE 5  
**Domain:** Aerospace | AI/ML | Space Situational Awareness

##  Overview

ORBITGUARD is a proposed AI-assisted space debris risk prediction system designed to identify, analyze, and prioritize potentially dangerous close approaches between objects in Earth's orbit.

Satellites, rocket bodies, and space debris continuously move through Earth's orbital environment. Predicting their future positions and identifying potentially hazardous encounters is challenging due to orbital uncertainty and changing data quality.

ORBITGUARD aims to combine physics-based orbital propagation with explainable risk scoring to help users understand which close approaches deserve attention first and why.

## Problem Statement

Thousands of artificial objects occupy Earth's orbit. Their future positions are uncertain, making it difficult to identify which close approaches could become dangerous.

Existing workflows may require operators to review many potential conjunction events. ORBITGUARD aims to simplify this process by screening orbital data, identifying close approaches, and prioritizing events using transparent risk indicators.

##  Proposed Solution

ORBITGUARD uses a lightweight, modular pipeline to process publicly available orbital data and identify potential close approaches.

The system is designed to:

- Load and validate orbital elements from public data sources.
- Predict future object positions using the SGP4 orbital propagation model.
- Screen object pairs for potential close approaches.
- Rank detected events using an explainable risk score.
- Display risk factors, uncertainty indicators, and alerts through an interactive dashboard.
- Evaluate prediction errors, detection performance, false alerts, and processing time.

Machine learning may be incorporated if suitable labelled data is available.

##  Key Features

- **Orbital Propagation:** Predict future positions of selected orbital objects.
- **Conjunction Screening:** Identify candidate close approaches between objects.
- **Explainable Risk Scoring:** Prioritize events based on separation, relative velocity, data freshness, and uncertainty indicators.
- **Interactive Dashboard:** Present orbital views, event tables, risk rankings, and explanations.
- **Data Quality Checks:** Validate orbital elements and highlight limitations associated with stale or uncertain data.
- **Performance Evaluation:** Assess position errors, detection precision and recall, false-alert rates, and processing time.

##  System Workflow

1. **Data Collection:** Load public orbital data, such as Two-Line Element (TLE) sets.
2. **Preprocessing:** Validate object identifiers, timestamps, and data quality.
3. **Orbit Propagation:** Use SGP4 to estimate future orbital positions.
4. **Conjunction Screening:** Identify candidate close approaches.
5. **Risk Analysis:** Calculate an explainable score and rank events.
6. **Visualization:** Display events, risk factors, uncertainty flags, and alerts.
7. **Evaluation:** Test the pipeline against reference data and clearly labelled synthetic scenarios.

## Technology Stack

| Component | Proposed Technologies |
|---|---|
| Programming Language | Python |
| Orbital Propagation | SGP4, Skyfield |
| Data Processing | NumPy, Pandas |
| Risk Analysis | Closest-approach screening, explainable scoring |
| AI/ML | Scikit-learn, if suitable labelled data is available |
| Dashboard | Streamlit, Plotly |
| Data Storage | CSV, SQLite |
| Orbital Data | CelesTrak TLEs; optional Space-Track data and historical Conjunction Data Messages (CDMs) |

##  System Architecture

**Public Orbital Data → Preprocessing → Orbit Propagation → Conjunction Screening → Risk Ranking and Explanation → Interactive Dashboard and Alerts**

Optional contextual data may include historical Conjunction Data Messages and space-weather information.

The system is designed as a lightweight prototype that can run without a GPU for its core processing pipeline.

## Expected Outcomes

The planned deliverables include:

- A working prototype using a bounded public TLE dataset.
- Orbital propagation and a close-approach event table.
- An explainable screening risk score.
- An interactive dashboard with orbital trajectories and event details.
- A short evaluation report and reproducible demonstration scenario.

## Evaluation Metrics

The prototype will be evaluated using:

- Predicted position error against reference data.
- Conjunction detection precision and recall.
- False-alert rate on test scenarios.
- Processing time for the selected object set.
- Correct identification and explanation of risk factors.

##  Limitations and Safety

- Prediction accuracy depends on the quality and age of the orbital data.
- Public TLE datasets generally do not provide the covariance information needed to establish a calibrated collision probability.
- The risk score is a screening and prioritization indicator, not a certified collision probability.
- Synthetic test cases will be labelled clearly.
- ORBITGUARD is a decision-support prototype and does not issue automatic spacecraft maneuver commands.

##  Team Members

**Team CORE 5**

- Siddangouda Patil
- Sudarshan Kulkarni
- Vaishakhi Waddinawar
- Vijita Patil
- Mahi Kulkarni

##  Future Scope

- Incorporate additional orbital datasets and historical conjunction information.
- Improve uncertainty-aware risk assessment when suitable data becomes available.
- Evaluate machine-learning methods using appropriate labelled datasets.
- Enhance interactive orbital visualization and scenario analysis.
- Extend testing to larger object sets and additional reference scenarios.

##  Project Status

Hackathon prototype — implementation, testing, and evaluation are planned as part of the project development process.

---

**Built by Team CORE 5 for Hackfest.**
