≈# Mapping AI Representation Gap
<<<<<<< HEAD
This repo contains data, code, and reports for analyzing AI representation gaps.

=======
 This repo contains data, code, and reports for analyzing AI representation gaps.
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)

---

## Project Overview
<<<<<<< HEAD

This project addresses the question: By building a hate speech detector, how can we measure performance disparities across demographic groups and identify which communities are underserved or over-policed? This is crucial as it aims to reveal potential algorithmic biases, ensuring that AI systems treat all demographic groups fairly and equitably. Identifying these disparities is vital for improving the accountability and transparency of AI technologies.

- **Objective:** Build a hate speech detector and measure performance disparities across demographic groups to identify which communities are underserved or over-policed  
- **Domain:** Bias in Artificial Intelligence 
- **Key Techniques:** 

---
=======
 This project addresses the question: By building a hate speech detector, how can we measure performance disparities across demographic groups and identify which communities are underserved or over-policed? This is crucial as it aims to reveal potential algorithmic biases, ensuring that AI systems treat all demographic groups fairly and equitably. Identifying these disparities is vital for improving the accountability and transparency of AI technologies.


 **Key Finding:** 
 - **Objective:** Build a hate speech detector and measure performance disparities across demographic groups to identify which communities are underserved or over-policed
 - **Domain:** Bias in Artificial Intelligence
 - **Key Techniques:** Data integration, cleaning, exploratory analysis, model training, model testing, regression modeling, statistical validation

--- 
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)

## Project Structure

```
<<<<<<< HEAD
├── data/                           # Raw and processed data
│   ├──                       
│   ├── 
│   ├── 
│   ├──                             # Cleaned datasets ready for analysis                
├── code/                           # Jupyter notebooks
│   ├──                             # Data loading, filtering, and outlier removal, exploratory
├── reports/                        # Generated reports and visualizations
│   └──                             # Complete analysis report
├── requirements.txt                # Python dependencies
└── README.md                       # Project documentation
=======
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)
```

---

## Data

<<<<<<< HEAD
We will utilize the following datasets:

[Jigsaw Civil Comments (Kaggle)](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data): Contains 2 million comments used to train the hate speech detector, featuring toxicity labels and identity mentions (race, religion, gender, disability).

[HateCheck (Paul Röttger GitHub)](https://github.com/paul-rottger/hatecheck-data): Provides 3,728 test cases for fairness benchmark testing, focusing on demographic variations.

[US Census 2020/2022](https://data.census.gov/): Offers demographic baseline comparisons, including population proportions by race, ethnicity, and disability.
- **License:** N/A

---
=======
- **Source:** Link to the data source(s) 
    - [Jigsaw Civil Comments(Kaggle)](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data) - 2M+ online comments with toxicity labels and sensitive identity attributes (race, gender, religion, disability). Used for training and evaluating the hate speech detector.
    - [Hatecheck Data (Paul Rottger GitHub)](https://github.com/paul-rottger/hatecheck-data) - 3,728 carefully constructed test cases designed to benchmark model robustness and fairness across demographic groups.
    - [US Census Data (2020/2022)](https://data.census.gov/) - Population proportions by race, ethnicity, and disability used to understand real-world representation and contextualize model bias findings.

- **Description:** 
    The combined datasets provide a large-scale, real-world corpus for training a hate speech detection model (Jigsaw), a controlled benchmark for fairness auditing across demographic groups (HateCheck), and population statistics for contextual demographic comparison (U.S. Census). The data was cleaned, merged, and transformed to prepare separate subsets for exploratory analysis, pilot training on a 10% sample, full-dataset model development, and fairness evaluation. 

--- 
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)

## Analysis


<<<<<<< HEAD

=======
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)
---

## Results


<<<<<<< HEAD

=======
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)
---

## Authors

<<<<<<< HEAD
- Prince Newman
- Bruna MacEdo Porto
- Maya Silver - [@mcsilver99](https://github.com/mcsilver99)
=======
- Bruna MacEdo Porto
- Maya Silver - @mcsilver99
- Prince Newman - @princenewman02
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)

---

## License

<<<<<<< HEAD
This project is licensed under the 

---

## Acknowledgements

- 
=======
---

## Acknowledgements
 - Python libraries: pandas, numpy, matplotlib, seaborn, scikit-learn
>>>>>>> d11f708 (Add initial notebooks, cleaned data, HateCheck test suite, census file, and project report; update README + requirements)
