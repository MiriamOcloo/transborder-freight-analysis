# transborder-freight-analysis
Data analysis project using CRISP-DM for BTS freight data

### Tools Used
- **Google Colab**: For data processing, visualization, and interactive development in Python.
- **Pandas**: To clean, manipulate, and aggregate the data.
- **Seaborn & Matplotlib**: To create visually appealing and insightful plots.
- **GitHub**: For version control and documentation.

---

### Dataset
The dataset was obtained from the [The Bureau of Transportation Statistics (BTS)](https://azubiafrica-my.sharepoint.com/:u:/g/personal/emmanuel_agyen_azubiafrica_org/EYddQyNqYidPuJW6qaNFxcABYaVfF-kZ14K2pJfHjKWmmg?e=wz822N) and includes monthly ZIP files for various months and years. The data spans 2020–2024 and includes trade metrics such as:

- VALUE (Trade Value)
- SHIPWT (Shipping Weight)
- FREIGHT_CHARGES
- COUNTRY (1220: Canada, 2010: Mexico)
- DISAGMOT (Transport Mode Codes)
- TRDTYPE (Trade Type: Export/Import)
- DF (Domestic/Foreign)
- USASTATE (US Border State)
- MONTH, YEAR

Reference documents and mapping dictionaries were used to convert code-based fields into readable formats.

---

### CRISP-DM Implementation

#### 1. Business Understanding
Key questions explored:

1. What are the top modes of transportation used for transborder trade by total value and shipping weight?
2. Which partner countries contribute most to trade in terms of value and volume?
3. How does the trade value and shipping weight vary across different months and years?
4. What’s the difference in total value, shipping weight, and freight charges between domestic and foreign produced merchandise?
5. Which transportation mode incurs the highest average freight charges?
6. Are there notable trends in freight movement across different U.S. border states over time?
7. What are the most common trade types (import/export), and how do their values and weights compare over time?

#### 2. Data Understanding
- Multi-year CSV data embedded in nested ZIP folders.
- Loaded using recursive directory search.
- Cleaned for nulls, inconsistent formats, and duplicated headers.

#### 3. Data Preparation
- Combined 50+ individual monthly datasets.
- Mapped code values (e.g., transport modes, countries, trade type).
- Parsed date columns and ensured proper data types for grouping and plotting.

#### 4. Modeling
- No machine learning models applied.
- Purely exploratory and visual analysis.

#### 5. Evaluation
- Grouped data by year, state, mode, country, and trade type.
- Created comparative and temporal visualizations.
- Applied consistent formatting, data labels, and legends for clarity.

#### 6. Deployment
- Visualizations rendered in Colab and saved/exported.
- Final presentation includes key insights.
- Codebase hosted on GitHub with this README and documented commits.

---

### Repository Structure

```bash
├── data/                  # Raw and processed data files
├── notebooks/             # Google Colab notebooks (.ipynb)
├── presentation/          # Final presentation file
├── visualizations/        # Exported chart images
└── README.md              # Project summary and documentation
