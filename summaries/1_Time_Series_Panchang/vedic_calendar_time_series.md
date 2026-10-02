# Paper Title: Natural Time-Series Analysis and Vedic Hindu Calendar System

* **Authors:** Neeraj Dhanraj Bokde 
* **Publication Year:** 2021
* **DOI / Link:** https://arxiv.org/abs/2111.03441
* **Category:** [1_Time_Series_Panchang]

---

### 🎯 1. Core Objective

* Addresses the limitations of using the Gregorian calendar for modeling natural phenomena, advocates Vedic Hindu calendar's lunisolar framework naturally captures the join influences of the sun and moon better than a solar-only calendar. Highlights lack of programmatic computational tools for this transition and presents a framework to bridge the gap.

### 📊 2. Data & Features Used

* **Dataset Source:** Historical meteorological profiles, socio-economic indicators, and astronomical positional calculations derived via ephemeris algorithms.
* **Key Features:** Traditional solar time tracking converted to the 5 parameters of the **Panchanga**: _Tithi_ (lunar phase), _Vaara_ (solar weekday), _Nakshatra_ (stellar constellation), _Yoga_ (sun-moon angular arc), and _Karana_ (half-tithi), alongside seasonal variables like _Ritu_ (seasons) and _Masa_ (lunar months).

### ⚙️ 3. Algorithms & Methodology

* **Models Used:** Time-series decomposition, correlation analysis, and linear regression models modified for cyclical adjustment.
* **Methodology Overview:** The authors engineered and evaluated the open-source [VedicDateTime R Framework](https://link.springer.com/article/10.1007/s11042-023-16553-w) to map irregular Gregorian intervals into 12 equal 30-degree coordinate-based segments. They calculated inter-month correlation coefficients and evaluated data variance after adjusting for moving lunisolar festival impacts like Diwali.

### 📈 4. Results & Findings

* **Best Performing Approach:** Time-series feature engineering utilizing the native Vedic coordinate calculations proved superior in aligning natural cycles compared to fixed Gregorian dates.
* **Key Findings:** Moving calendar boundaries in standard software induce structural temporal distortions. The Vedic system eliminates these distortions by tying time variables directly to true astronomical coordinates, yielding **stronger inter-month correlation coefficients** across natural time-series data sets.

### 💡 5. Project Relevance 

* **Direct Application:** This paper provides the exact mathematical foundation and code validation framework needed for this project. By utilizing their [VedicDateTime repository](https://rpubs.com/prajwalpatil/VedicDateTime), we can convert the standard "Month/Day" variables in our forest fire dataset into _Tithis_, _Lagnas_, and _Ritus_. Because forest fire variables like relative humidity, wind velocity, and vegetative moisture are heavily driven by tidal and solar-lunar cycles, tracking time through _Tithis_ instead of artificial Gregorian months will allow machine learning models (like Random Forest or XGBoost) to extract cleaner cyclical features, ultimately **improving early-stage fire risk accuracy**.