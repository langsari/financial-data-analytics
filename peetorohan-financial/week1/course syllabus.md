# 📈 DS2303-425: Financial Data Analytics

[![Course Code](https://img.shields.io/badge/Course-DS2303--425-blue.svg)](#)
[![Prerequisite](https://img.shields.io/badge/Prerequisite-DS2303--420%20Machine%20Learning-orange.svg)](#)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](#)
[![Credits](https://img.shields.io/badge/Credits-3%20(2--2--5)-success.svg)](#)
[![Status](https://img.shields.io/badge/Curriculum-Modernized%202026-brightgreen.svg)](#)

> **Official Course Syllabus, Curriculum Modernization Roadmap & Practical Lab Repository**  
> หลักสูตรวิทยาศาสตรบัณฑิต สาขาวิชาวิทยาการข้อมูลและการวิเคราะห์เชิงธุรกิจ (Data Science and Business Analytics)

---

## 🎯 1. ภาพรวมและคำอธิบายรายวิชา (Course Overview & Description)

| ข้อมูลรายวิชา | รายละเอียด |
| :--- | :--- |
| **รหัสและชื่อรายวิชา (TH)** | `DS2303-425` การวิเคราะห์ข้อมูลทางการเงิน |
| **รหัสและชื่อรายวิชา (EN)** | `DS2303-425` Financial Data Analytics |
| **รายวิชาบังคับก่อน** | `DS2303-420` การเรียนรู้ของเครื่อง (Machine Learning) |
| **จำนวนหน่วยกิต** | `3 (2-2-5)` หน่วยกิต |

### คำอธิบายรายวิชา (Course Description)
* **ภาษาไทย:** แนวคิดและภาพรวมของการวิเคราะห์ข้อมูลทางการเงินสมัยใหม่ โครงสร้างและลักษณะเฉพาะทางสถิติของข้อมูลทางการเงิน การดึงและการเตรียมข้อมูลทางการเงินจากแหล่งข้อมูลจริงและข้อมูลทางเลือก การวิเคราะห์ข้อมูลอนุกรมเวลาทางการเงิน การสร้างและการประเมินประสิทธิภาพของแบบจำลองการพยากรณ์ทั้งเชิงสถิติและการเรียนรู้ของเครื่อง การวัดความผันผวน ราคา ผลตอบแทน และความเสี่ยงของสินทรัพย์ทางการเงิน ทฤษฎีพอร์ตโฟลิโอสมัยใหม่และการจัดสรรสินทรัพย์เชิงปริมาณ การทดสอบกลยุทธ์การลงทุนย้อนหลัง ตลอดจนการประยุกต์ใช้เทคนิคการเรียนรู้ของเครื่องและการประมวลผลภาษาธรรมชาติในบริบททางธุรกิจการเงิน เช่น การประเมินความเสี่ยงด้านสินเชื่อ และการตรวจจับการทุจริตทางการเงิน
* **English:** Concepts and overview of modern financial data analytics; structure and stylized facts of financial data; acquisition and preprocessing of real-world financial and alternative data; financial time-series analysis; development and performance evaluation of statistical and machine learning forecasting models; analysis of volatility, asset pricing, returns, and financial risks; modern portfolio theory and quantitative asset allocation; algorithmic strategy backtesting; and applications of machine learning and natural language processing in financial business contexts, including credit risk scoring and financial fraud detection.

---

## 🔄 2. การปรับปรุงหลักสูตรสู่มาตรฐานปัจจุบัน (Curriculum Modernization)

เพื่อให้รายวิชาสอดคล้องกับอุตสาหกรรม **FinTech**, **Quantitative Finance** และความต้องการของตลาดแรงงานในปัจจุบัน จึงได้ปรับปรุงเนื้อหาจากหลักสูตรดั้งเดิมดังนี้:

| มิติการพัฒนา | ❌ สิ่งที่ตัดออก / ลดทอน | ✅ สิ่งที่เพิ่มเติม / ปรับปรุงใหม่ | 💡 เหตุผลเชิงวิชาการและอุตสาหกรรม |
| :--- | :--- | :--- | :--- |
| **เครื่องมือวิเคราะห์** | ตัดการสร้างโมเดลทางการเงินด้วย Spreadsheet (Excel) แบบดั้งเดิม | ใช้ **Python Quantitative Stack** (`pandas`, `statsmodels`, `arch`, `PyPortfolioOpt`, `quantstats`) | รองรับข้อมูลขนาดใหญ่ ดึงข้อมูลผ่าน API อัตโนมัติ และต่อยอดสู่ระบบ Production ได้จริง |
| **การวิเคราะห์อนุกรมเวลา** | ลดการพิสูจน์คณิตศาสตร์เชิงลึกของกระบวนการ Box-Jenkins ด้วยมือ | เพิ่มการทดสอบความนิ่ง (`ADF`/`KPSS`), **GARCH** (Volatility) และ **ML/DL Time-Series** (`XGBoost`, `LSTM`) | ตลาดการเงินมีความสัมพันธ์ไม่เชิงเส้นและมีความผันผวนแบบเกาะกลุ่ม (*Volatility Clustering*) |
| **การตรวจสอบโมเดล** | ตัดการใช้ Random Split และ K-Fold Cross-Validation แบบมาตรฐาน | ใช้ **Walk-Forward Validation** และ **Purged Group Time-Series Split** | ป้องกันอคติจากการมองเห็นข้อมูลอนาคต (*Look-ahead Bias* & *Data Leakage*) |
| **พอร์ตโฟลิโอและความเสี่ยง** | ลดการพึ่งพาค่าเบี่ยงเบนมาตรฐาน (SD) เพียงอย่างเดียวในการวัดความเสี่ยง | เพิ่ม **Sharpe, Sortino, Max Drawdown**, **Fama-French** และ **VaR / CVaR** | ผลตอบแทนทางการเงินมีลักษณะหางอ้วน (*Fat Tails*) การใช้ SD ต่ำกว่าความเสี่ยงจริงในภาวะวิกฤต |
| **การประยุกต์ใช้ทางธุรกิจ** | ยกเลิกหัวข้อกว้างๆ ("เทคนิคการวิเคราะห์ในบริบทอื่นๆ") | กำหนด 3 เสาหลักยุคใหม่: **Algorithmic Backtesting**, **Credit/Fraud ML**, และ **Financial NLP (`FinBERT`)** | เชื่อมโยงอัลกอริทึมจากวิชา ML สู่โจทย์ธุรกิจจริงของสถาบันการเงินยุคดิจิทัล |

---

## 🔗 3. การเชื่อมโยงองค์ความรู้จากวิชาบังคับก่อน (Prerequisite Mapping)

การต่อยอดอัลกอริทึมจากรายวิชา **DS2303-420 Machine Learning** สู่โจทย์ทางการเงินในรายวิชา **DS2303-425**:

```text
[DS2303-420: Machine Learning]                 [DS2303-425: Financial Data Analytics]
─────────────────────────────────              ──────────────────────────────────────────
• Linear Regression & OLS              ───►    • CAPM & Fama-French Multi-Factor Models (Alpha/Beta)
• Logistic Regression                  ───►    • Credit Risk Scoring & Probability of Default (PD)
• Neural Networks (MLP / Deep)         ───►    • Recurrent Neural Networks (LSTM) for Price/Volatility
• K-Nearest Neighbors (KNN) & SVM      ───►    • Market Regime Classification & Trading Signal Generation
• K-Means Clustering                   ───►    • Asset Clustering & Hierarchical Risk Parity (HRP)
• Expectation-Maximization (EM / GMM)  ───►    • Anomaly Detection & Hidden Market State Identification
• Principal Component Analysis (PCA)   ───►    • Yield Curve Modeling & Statistical Factor Extraction
• Cross-Validation & Evaluation        ───►    • Walk-Forward Validation, Backtesting & Risk Metrics
```

---

## 🎓 4. ผลลัพธ์การเรียนรู้ของรายวิชา (Course Learning Outcomes)

* **`CLO1` วิศวกรรมข้อมูลทางการเงิน (Financial Data Engineering):** อธิบายลักษณะเฉพาะทางสถิติของข้อมูลทางการเงิน (*Stylized Facts*) และดำเนินการดึงข้อมูล ทำความสะอาด รวมถึงสร้างตัวแปรเชิงปริมาณ (*Quantitative Feature Engineering*) จากข้อมูลตลาดการเงินจริงได้อย่างถูกต้อง
* **`CLO2` การวิเคราะห์อนุกรมเวลาและการพยากรณ์ (Time-Series & Forecasting):** วิเคราะห์โครงสร้างข้อมูลอนุกรมเวลา พัฒนาแบบจำลองพยากรณ์ทั้งเชิงสถิติ (`ARIMA`, `GARCH`) และการเรียนรู้ของเครื่อง (`ML/DL`) พร้อมประเมินประสิทธิภาพภายใต้กรอบการตรวจสอบที่ปราศจากอคติ (*Leakage-Free Validation*)
* **`CLO3` การบริหารพอร์ตโฟลิโอและความเสี่ยง (Portfolio & Risk Management):** วิเคราะห์ความสัมพันธ์ระหว่างผลตอบแทนและความเสี่ยง ประยุกต์ใช้ทฤษฎีพอร์ตโฟลิโอสมัยใหม่ร่วมกับอัลกอริทึมการหาค่าเหมาะสมที่สุดและการจัดกลุ่มข้อมูล เพื่อจัดสรรสินทรัพย์และบริหารความเสี่ยง
* **`CLO4` การประยุกต์ใช้เชิงธุรกิจและนวัตกรรม (Applied Financial AI):** บูรณาการเทคนิคการเรียนรู้ของเครื่องและการประมวลผลภาษาธรรมชาติ เพื่อออกแบบ พัฒนา และทดสอบระบบสนับสนุนการตัดสินใจทางการเงินในสถานการณ์จริง

---

## 🗓️ 5. แผนการจัดการเรียนรู้ 15 สัปดาห์ (15-Week Course Roadmap)

### 📦 Module 1: รากฐานข้อมูลทางการเงินและวิศวกรรมตัวแปร (Weeks 1–3)
| สัปดาห์ | หัวข้อบรรยาย (Lecture) | ปฏิบัติการ (Hands-on Lab) |
| :---: | :--- | :--- |
| **01** | **Modern Financial Data Analytics Ecosystem**<br>โครงสร้างตลาดการเงิน ประเภทสินทรัพย์ และบทบาทของ Quant | `Lab 01`: ดึงข้อมูลราคาหลักทรัพย์และตัวชี้วัดเศรษฐกิจผ่าน API (`yfinance`, `fredapi`) |
| **02** | **Stylized Facts & Data Preprocessing**<br>Simple vs. Log Returns, Fat Tails, Skewness, Kurtosis, Volatility Clustering | `Lab 02`: Resampling ข้อมูล, การปรับฐาน Corporate Actions และทดสอบ Stylized Facts |
| **03** | **Quantitative Feature Engineering & PCA**<br>ตัวชี้วัดทางเทคนิค/ปัจจัยพื้นฐาน และการใช้ **PCA** ลดมิติและสกัดปัจจัยเสี่ยง | `Lab 03`: สร้าง Feature Matrix และทำ PCA วิเคราะห์โครงสร้างความแปรปรวนหุ้น SET50 |

### 📈 Module 2: การวิเคราะห์อนุกรมเวลาและการพยากรณ์ทางการเงิน (Weeks 4–7)
| สัปดาห์ | หัวข้อบรรยาย (Lecture) | ปฏิบัติการ (Hands-on Lab) |
| :---: | :--- | :--- |
| **04** | **Time-Series Decomposition & Stationarity**<br>องค์ประกอบอนุกรมเวลา, Unit Root (`ADF`/`KPSS`), Differencing & Fractional Diff | `Lab 04`: ทดสอบความนิ่ง แปลงข้อมูลให้ Stationary และวิเคราะห์กราฟ ACF / PACF |
| **05** | **Statistical Forecasting: ARMA & ARIMA**<br>แบบจำลอง AR, MA, ARMA, ARIMA, เกณฑ์ AIC/BIC และ Auto-ARIMA | `Lab 05`: พัฒนาโมเดล ARIMA พยากรณ์อัตราแลกเปลี่ยน พร้อมทำ Residual Diagnostics |
| **06** | **Volatility Modeling: ARCH & GARCH**<br>ความสำคัญของการพยากรณ์ความผันผวน, ทฤษฎี ARCH, GARCH(1,1) และ EGARCH | `Lab 06`: ทดสอบ ARCH Effect และใช้ไลบรารี `arch` พยากรณ์ความผันผวนรายวัน |
| **07** | **ML Forecasting & Walk-Forward Validation**<br>Sliding Window, **Regression, SVM, LSTM**, XGBoost และ **Walk-Forward Validation** | `Lab 07`: เปรียบเทียบโมเดลสถิติ vs. ML/DL ภายใต้ระบบ Walk-Forward Validation |

> 📝 **Week 08: Midterm Examination** (ประเมินผลเนื้อหา Module 1 – 2 ครอบคลุม `CLO1` และ `CLO2`)

### 💼 Module 3: ทฤษฎีพอร์ตโฟลิโอและการบริหารความเสี่ยงเชิงปริมาณ (Weeks 9–11)
| สัปดาห์ | หัวข้อบรรยาย (Lecture) | ปฏิบัติการ (Hands-on Lab) |
| :---: | :--- | :--- |
| **09** | **Modern Portfolio Theory & Optimization**<br>ทฤษฎี Markowitz, Covariance Matrix, Efficient Frontier, Min-Vol & Max-Sharpe | `Lab 08`: จำลองพอร์ตโฟลิโอด้วย Monte Carlo และหาสัดส่วนเหมาะสมด้วย `PyPortfolioOpt` |
| **10** | **Asset Pricing & Asset Clustering**<br>CAPM (**OLS**), Fama-French Factors และการจัดกลุ่มสินทรัพย์ (**K-Means**, Hierarchical) | `Lab 09`: วิเคราะห์ Alpha/Beta กองทุนรวมด้วย Fama-French และจัดกลุ่มสินทรัพย์ |
| **11** | **Performance Attribution & Risk Management**<br>Sharpe, Sortino, Calmar, Max Drawdown และความเสี่ยงด้านลบ (**VaR & CVaR**) | `Lab 10`: สร้างรายงานวิเคราะห์พอร์ตระดับสถาบันด้วย `quantstats` และทำ Stress Testing |

### 🚀 Module 4: การประยุกต์ใช้ขั้นสูงในธุรกิจการเงินยุคใหม่ (Weeks 12–15)
| สัปดาห์ | หัวข้อบรรยาย (Lecture) | ปฏิบัติการ (Hands-on Lab) |
| :---: | :--- | :--- |
| **12** | **Algorithmic Trading & Backtesting**<br>สร้างสัญญาณซื้อขาย (**KNN, SVM**), ต้นทุนแฝง (Slippage/Commission) และ Overfitting | `Lab 11`: สร้างกลยุทธ์การลงทุนเชิงปริมาณและทำ Backtesting เทียบกับ Buy & Hold |
| **13** | **Credit Scoring & Fraud Detection**<br>Credit Scoring (**Logistic Regression**, WoE/IV) และ Fraud Detection (**EM/GMM**) | `Lab 12`: พัฒนาโมเดลทำนายการผิดนัดชำระหนี้และการตรวจจับธุรกรรมทุจริต |
| **14** | **Alternative Data & Financial NLP**<br>ข้อมูลทางเลือกและการวิเคราะห์ความเชื่อมั่นข่าวการเงินด้วย **FinBERT / LLMs** | `Lab 13`: สกัด Sentiment Index จากข่าวการเงินด้วย FinBERT และวิเคราะห์ผลต่อตลาด |
| **15** | **Capstone Project Presentation**<br>นำเสนอโครงงานบูรณาการการวิเคราะห์ข้อมูลทางการเงินจากโจทย์ธุรกิจจริง | `Capstone`: นำเสนอผลงาน โค้ดต้นแบบ และรายงานฉบับสมบูรณ์ |

---

## 📊 6. เกณฑ์การวัดและประเมินผล (Assessment & Grading)

| Assessment Component | Weight | Evaluation Criteria and Deliverables |
| :--- | :---: | :--- |
| **1. Weekly Practical Labs (13 Labs)** | **25%** | Reproducible Jupyter Notebooks (`.ipynb`) covering API data pipelines, statistical tests (`ADF`/`KPSS`), `ARIMA`/`GARCH` modeling, and financial interpretation |
| **2. Midterm Examination** | **25%** | Closed-book analytical exam evaluating mastery of financial stylized facts, stationarity transformations, volatility modeling, and leakage-free validation |
| **3. Mini-Project (Capstone Phase 1)** | **15%** | Automated data ingestion script, Exploratory Data Analysis (EDA) notebook, and baseline forecasting model with strict prevention of look-ahead bias |
| **4. Final Integrated Model & Code** | **20%** | Production-ready GitHub repository, algorithmic strategy backtesting (`Sharpe`/`Sortino`/`Max Drawdown`), transaction cost modeling, and `SHAP` explainability |
| **5. Capstone Technical Report & Defense** | **15%** | A 12–15 page academic technical report detailing methodology and risk-adjusted results, paired with a live system demonstration and executive Q&A defense |

This distribution prevents last-minute cramming by rewarding consistent weekly lab execution and phased project milestones while maintaining high standards for leakage-free modeling and financial risk evaluation.



## 📚 7. ตำราและแหล่งอ้างอิง (References & Resources)

### ตำราหลัก (Required Textbooks)
1. **López de Prado, M.** (2018). *Advances in Financial Machine Learning*. John Wiley & Sons.
2. **Jansen, S.** (2020). *Machine Learning for Algorithmic Trading* (2nd ed.). Packt Publishing.
3. **Tsay, R. S.** (2010). *Analysis of Financial Time Series* (3rd ed.). John Wiley & Sons.

### ตำราอ่านประกอบเพิ่มเติม (Recommended Readings)
4. **Dixon, M. F., Halperin, I., & Bilokon, P.** (2020). *Machine Learning in Finance: From Theory to Practice*. Springer.
5. **Hilpisch, Y.** (2018). *Python for Finance: Mastering Data-Driven Finance* (2nd ed.). O'Reilly Media.
6. **Bodie, Z., Kane, A., & Marcus, A. J.** (2021). *Investments* (12th ed.). McGraw-Hill Education.