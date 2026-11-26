# Integrated Project-Based Learning (iPBL) Framework: DS2303-420 Machine Learning and DS2303-425 Financial Data Analytics

Modern data science education depends on pairing theoretical foundations with authentic domain application rather than teaching algorithms and industry problems in isolation. Within the Department of Data Science and Analytics (International Program), Faculty of Science and Technology at Fatoni University, the **Integrated Project-Based Learning (iPBL)** framework unites **DS2303-420 Machine Learning** and **DS2303-425 Financial Data Analytics** into a cohesive six-credit learning experience. This document synthesizes the curriculum rationale, cross-course content mapping, 16-week capstone sprint architecture, Agile laboratory workflow, authentic assessment rubric, and strategic execution plan established for Semester 2/2569.

---

## 1. Unifying Theory and Domain Practice Through a Six-Credit Structure

Delivering **DS2303-420 Machine Learning** (3 credits, 2-2-5) and **DS2303-425 Financial Data Analytics** (3 credits, 3-0-6) in the same academic term creates an uncommon structural advantage. Because **Ajarn Khalid Langsari** teaches both courses to the exact same student cohorts—Groups **DS671** and **DS672**—the curriculum can eliminate redundant instruction and replace siloed assignments with a single **Authentic Capstone Project** worth six combined credits. Under this model, students treat supervised and unsupervised machine learning not as abstract mathematical exercises, but as operational instruments for solving time-series forecasting, asset pricing, and portfolio management problems.

To clarify how the two courses interlock logistically and pedagogically, the table below summarizes their core administrative and instructional parameters as defined in the framework.

| Parameter | DS2303-420 Machine Learning | DS2303-425 Financial Data Analytics |
| :--- | :--- | :--- |
| **Credit Structure** | 3 Credits (2-2-5) | 3 Credits (3-0-6) |
| **Semester & Cohorts** | Semester 2/2569 — Groups DS671 & DS672 | Semester 2/2569 — Groups DS671 & DS672 |
| **Instructor** | Ajarn Khalid Langsari | Ajarn Khalid Langsari |
| **Scheduled Days** | Tuesday and Sunday | Wednesday and Thursday |
| **Primary Pedagogical Role** | Core ML theory, algorithms, and evaluation | Financial domain application and Programming Lab project work |

By aligning both courses under one instructional arc, every algorithmic concept introduced in Machine Learning immediately feeds into a concrete financial modeling task in Financial Data Analytics.

---

## 2. Aligning Financial Analytics With Machine Learning Algorithms

A central strength of the iPBL framework is that it maps each major financial analytics topic directly onto corresponding machine learning methods, ensuring that neither subject outpaces the other. Rather than waiting until the end of the semester to connect the two disciplines, students continuously pair statistical finance techniques with data-driven algorithms across four core thematic pillars.

The matrix below details how financial domain topics from **DS2303-425** pair with machine learning algorithms from **DS2303-420** to produce integrated capstone capabilities.

| Financial Analytics Topic (DS2303-425) | Machine Learning Algorithms (DS2303-420) | Integrated iPBL Application |
| :--- | :--- | :--- |
| **Time Series Analytics** | Linear Regression, Least Squares, PCA, Feature Engineering | Preparing stock price datasets, reducing dimensionality with Principal Component Analysis (PCA), and engineering predictive features |
| **ARIMA Forecasting & Performance Measurement** | Artificial Neural Networks (ANN), Support Vector Machines (SVM), Cross-Validation | Benchmarking traditional ARIMA forecasts against machine learning models (SVR and ANN) using Cross-Validation |
| **Modern Portfolio Theory (MPT)** | K-Means Clustering, Expectation-Maximization (EM) Algorithm | Grouping assets and stocks by risk profiles and behavioral patterns via K-Means and EM prior to calculating portfolio weights |
| **Risk-Return Evaluation** | Logistic Regression, K-Nearest Neighbors (KNN), Model Evaluation Metrics | Classifying market movement directions (Up/Down Trend) and stratifying risk tiers through classification techniques |

This cross-disciplinary pairing transforms how students evaluate models: they learn not only whether an algorithm minimizes statistical error, but also whether its outputs support sound financial decision-making.

---

## 3. The 16-Week Capstone Architecture: AI-Driven Financial Forecasting and Dynamic Portfolio Optimization

Throughout the 16-week semester, student teams execute a single end-to-end capstone project titled **"AI-Driven Financial Forecasting & Dynamic Portfolio Optimization"** (*ระบบพยากรณ์อนุกรมเวลาทางการเงินและการจัดพอร์ตการลงทุนอัจฉริยะ*). The project is structured into four sequential four-week Sprints, each escalating in analytical complexity from raw market data ingestion to an interactive backtesting web application.

### Sprint 1 (Weeks 1–4): Data Acquisition, Preprocessing, and Market Clustering

The opening Sprint establishes a clean, structured financial dataset and segments the investment universe before any predictive modeling begins. Students combine financial return calculations with unsupervised learning to understand asset behavior across market groups.

* **Financial Objectives**: Retrieve historical prices for stocks, assets, or financial indices, and compute asset returns and volatility.
* **Machine Learning Objectives**: Clean raw datasets, handle missing data, apply Principal Component Analysis (PCA) for dimensionality reduction, and use K-Means Clustering to group stocks with similar risk characteristics.
* **Required Deliverable**: Exploratory Data Analysis (EDA) Report and Stock Clustering Notebook.

### Sprint 2 (Weeks 5–8): Time Series Analysis and Baseline Forecasting

Once the asset universe is organized, Sprint 2 establishes rigorous forecasting benchmarks. Students test whether classical econometric models or baseline machine learning regressors capture price dynamics more effectively under proper temporal validation.

* **Financial Objectives**: Test and analyze time-series stationarity, build ARIMA forecasting models, and measure predictive error using RMSE, MAE, and MAPE.
* **Machine Learning Objectives**: Construct Linear Regression and Support Vector Regression (SVR) baseline models, evaluating them with Time-Series Cross-Validation.
* **Required Deliverable**: Time-Series Forecasting Benchmark Report comparing ARIMA against ML Baselines.

### Sprint 3 (Weeks 9–12): Complex Predictive Models and Risk Classification

Building on continuous price forecasts, Sprint 3 shifts focus toward directional market prediction and risk-regime classification. Students deploy non-linear and neural architectures to classify market trends and evaluate classification trade-offs.

* **Financial Objectives**: Classify market trend directions and analyze underlying risk regimes.
* **Machine Learning Objectives**: Apply Logistic Regression, K-Nearest Neighbors (KNN), and Artificial Neural Networks (ANN) to predict price direction, assessing classification performance with Confusion Matrices and F1-Scores.
* **Required Deliverable**: Deep Machine Learning and Trend Classification Suite.

### Sprint 4 (Weeks 13–16): Portfolio Optimization and Interactive Dashboard

The final Sprint synthesizes all prior clustering, forecasting, and classification outputs into an actionable portfolio engine and user-facing web interface. Students validate their integrated system through historical backtesting and formal academic presentation.

* **Financial Objectives**: Compute the Efficient Frontier under Modern Portfolio Theory (MPT) and optimize portfolio asset allocations using the Sharpe Ratio.
* **Machine Learning and Systems Integration Objectives**: Integrate ML forecasting outputs into the portfolio optimization engine and build a Web Dashboard to execute and visualize backtesting.
* **Required Deliverables**: Capstone Interactive Web Dashboard, Integrated Technical Report, and Team Presentation.

Together, these four Sprints ensure that every deliverable from earlier weeks becomes a direct input to the final portfolio optimization system.

---

## 4. Agile Laboratory Pedagogy and Industry-Standard Toolstack

To mirror real-world quantitative data science teams, the framework embeds **Agile/Scrum** practices directly into laboratory sessions across **Room 13-303 (IT Laboratory)** and **Room 13-304 (Programming Laboratory)**. Instructors facilitate structured **Sprint Planning**, **Standup Meetings**, and **Code Reviews** so that students receive continuous feedback rather than waiting until final exams to discover technical flaws.

Within each project team, students divide responsibilities across four defined operational roles:

1. **Data Engineer**: Manages data acquisition pipelines, missing-value imputation, and feature engineering workflows.
2. **Quant Analyst**: Leads financial return/volatility calculations, stationarity testing, ARIMA modeling, and Modern Portfolio Theory optimization.
3. **ML Engineer**: Designs, tunes, and validates supervised and unsupervised machine learning models, including SVR, KNN, K-Means, PCA, and ANN.
4. **Scrum Master**: Coordinates sprint timelines, facilitates standups, tracks deliverables, and ensures team integration across both courses.

Supporting these roles is a unified, industry-standard Python ecosystem organized into four functional layers, as outlined below.

* **Data Access and Processing**: Python with `Pandas`, `NumPy`, and the `yfinance` API for programmatic financial data retrieval and tabular manipulation.
* **Statistical and Financial Modeling**: `Statsmodels` for ARIMA time-series analysis and `PyPortfolioOpt` for Modern Portfolio Theory (MPT) portfolio optimization.
* **Machine Learning and AI**: `Scikit-Learn` (covering Regression, KNN, SVM, K-Means, PCA, and evaluation metrics) alongside `TensorFlow` or `PyTorch` for Artificial Neural Networks (ANN).
* **Dashboard and Visualization**: `Matplotlib`, `Seaborn`, `Plotly`, and `Streamlit` for analytical plotting and interactive backtesting web dashboards.

Standardizing on this single Python stack eliminates friction between theoretical lab exercises and final web dashboard deployment.

---

## 5. Authentic Assessment Framework Across Both Courses

Because the capstone project spans both **DS2303-420** and **DS2303-425**, evaluation is unified under a single 100% **Authentic Assessment Framework**. Grading balances continuous iterative progress (30%) against final technical rigor (35%), written academic communication (20%), oral defense (10%), and Agile team accountability (5%).

The table below specifies the five assessment components, their exact weightings, and the evaluation criteria applied across both courses.

| Assessment Component | Weight | Evaluation Criteria and Deliverables |
| :--- | :---: | :--- |
| **1. Continuous Sprint Deliverables** | 30% | Source code reviews (Code Review), Sprint 1–3 progress presentations, and completeness of intermediate sub-models |
| **2. Final Integrated Model & Code** | 35% | Algorithmic correctness of ML implementations, forecasting performance (Accuracy/RMSE), and completeness of the portfolio optimization system |
| **3. Integrated Capstone Technical Report** | 20% | A 12–15 page academic technical report detailing theoretical foundations, experimental methodology, and in-depth analytical results |
| **4. Capstone Presentation & Q&A** | 10% | Effectiveness of the team presentation, live system demonstration, and academic Q&A defense before qualified evaluators |
| **5. Peer Evaluation & Teamwork** | 5% | Evaluation of intra-team collaboration, workload distribution, and active participation under Agile principles |

This distribution prevents last-minute cramming by rewarding disciplined Sprint execution while maintaining high standards for final model accuracy and academic reporting.

---

## 6. Strategic Schedule Integration and Pathways to Academic Excellence

Operationalizing this six-credit iPBL model requires deliberate weekly coordination between the two courses' timetables and a clear pathway for high-performing teams to extend their work beyond the classroom.

First, **weekly schedule integration** leverages the complementary timing of both courses. The **Tuesday and Sunday** sessions for **DS2303-420 Machine Learning** focus on instilling core machine learning theory, mathematical intuition, and algorithmic mechanics. Immediately following, the **Wednesday and Thursday** sessions for **DS2303-425 Financial Data Analytics** concentrate on financial domain application and hands-on capstone project execution in the Programming Laboratory.

Second, **pathways to academic and competitive excellence** extend the capstone lifecycle past Week 16. Faculty are encouraged to mentor standout student teams to adapt their **12–15 page** technical reports and interactive backtesting dashboards for **Financial Data Science Competitions** or submit their findings for publication in **undergraduate academic venues**.
