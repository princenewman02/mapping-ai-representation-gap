# Mapping AI Representation Gap
  This repo contains data, code, and reports for analyzing AI representation gaps.

---

## Project Overview

    This project addresses the question: By building a hate speech detector, how can we measure performance disparities across demographic groups and identify which communities are underserved or over-policed? This is crucial as it aims to reveal potential algorithmic biases, ensuring that AI systems treat all demographic groups fairly and equitably. Identifying these disparities is vital for improving the accountability and transparency of AI technologies.

   - **Objective:** Build a hate speech detector and measure performance disparities across demographic groups to identify which communities are underserved or over-policed  
   - **Domain:** Bias in Artificial Intelligence 
   - **Key Techniques:** 

---

## Project Structure

    ```
    ├── data/                 # Raw and processed data
    ├── code/                 # Jupyter notebooks and Python scripts
    ├── reports/              # Generated reports and visualizations
    ├── requirements.txt      # Dependencies
    └── README.md             # Project documentation
    ```

---

## Data

We will utilize the following datasets:
   - **Source:** Link to the data source(s) 
        - [Jigsaw Civil Comments(Kaggle)](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data) 
        - [Hatecheck Data (Paul Rottger GitHub)](https://github.com/paul-rottger/hatecheck-data) 

   - **Description:** 
        The combined datasets provide a large-scale, real-world corpus for training a hate speech detection model (Jigsaw), and a controlled benchmark for fairness auditing across demographic groups (HateCheck). 
        - Jigsaw: Contains 2 million comments used to train the hate speech detector, featuring toxicity labels and identity mentions (race, religion, gender, disability).
        - Hatecheck: Provides 3,728 test cases for fairness benchmark testing, focusing on demographic variations.

--- 


## Analysis
**Identity & Toxicity Analysis Summary**
    Our exploration of the dataset revealed several structural imbalances that collectively increase the risk of model bias:
  - Representation Imbalance: Mentions of majority identities (e.g., female, male, Christian, white) dominated the dataset, while many minority and disability groups appeared in fewer than 0.03% of comments, limiting model exposure to these groups.

  - Toxicity Disparities: Underrepresented identities—especially LGBTQ+ groups—showed the highest average toxicity scores, while majority identities showed the lowest. This indicates that toxicity labels reflect skewed conversational patterns, not inherent harmfulness.

  - Biased Toxicity Rates: Some identities (e.g., black, bisexual, gay_or_lesbian) had toxic rates above 23%, compared to as low as 9% for groups like christian, suggesting label bias embedded in the data.

  - Sample Size Gaps: Many marginalized identities had fewer than 100 examples, providing too little data for a model to learn nuanced patterns and reinforcing the negative associations present.

  - Sparse Identity Interactions: Co-occurrence analysis showed majority groups appearing frequently together, while minority groups were isolated, revealing uneven relational structure in the dataset.

  - Overall Pattern: High frequency + low toxicity dominated majority identities, while low frequency + high toxicity characterized marginalized groups. This combination confirms systemic representation and labeling bias that models will inherit without corrective intervention.

---

## Results
    This study addressed whether a hate speech detection model trained on standard real-world data would exhibit demographic fairness. By training a DistilBERT classifier on 1.8 million Jigsaw Civil Comments and evaluating performance across 11 identity groups (excluding categories with insufficient sample sizes) using both observational (Jigsaw validation) and controlled (HateCheck) methods, we demonstrated significant algorithmic bias—not primarily in protection, but in surveillance burden. Our key findings are:
        1. Adequate but unequal protection. Detection rates across identity groups ranged from 80.8% to 93.2% in Jigsaw validation, indicating the model provides reasonable hate speech detection for all demographics.

        2. Severe over-policing disparities. False positive rates ranged from 13.2% (Christians) to 51.0% (Black people)—a 37.8 percentage point gap. Discussions mentioning Black Americans are flagged as toxic over half the time, even when benign.

        3. Systematic bias confirmed. Cross-dataset correlation between Jigsaw and HateCheck detection rates (r = 0.87, p < 0.01) demonstrates these patterns are embedded in the model itself, not artifacts of specific datasets.

        4. Training data origins identified. Exploratory analysis traced disparities to training data composition: groups frequently mentioned in toxic contexts become associated with toxicity, causing disproportionate false positives.

        These findings have concrete implications. When deployed at scale, such models impose vastly unequal costs: communities already targeted by hate speech face an additional burden of having their benign content disproportionately censored. The 98% false positive rate for Black identity terms in HateCheck's controlled testing represents near-complete silencing of any discussion mentioning Black People.

---

## Authors

  - Prince Newman (Data Lead) - [@princenewman02](https://github.com/princenewman02)
  - Bruna MacEdo Porto (Modeling Lead) 
  - Maya Silver - [@mcsilver99](https://github.com/mcsilver99)

---

## License:  
 N/A

---

## Acknowledgements/References

    Borkan, D., Dixon, L., Sorensen, J., Thain, N., & Vasserman, L. (2019). Nuanced metrics for measuring unintended bias with real data for text classification.  In Companion Proceedings of The 2019 World Wide Web Conference (pp. 491-500). 
    https://doi.org/10.1145/3308560.3317593

    Mozafari, M., Farahbakhsh, R., & Crespi, N. (2020). Hate speech detection and racial bias mitigation in social media based on BERT model. PloS one, 15(8), e0237861. https://doi.org/10.1371/journal.pone.0237861

    Röttger, P., Vidgen, B., Nguyen, D., Waseem, Z., Margetts, H., & Pierrehumbert, J. (2021). HateCheck: Functional tests for hate speech detection models. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers) (pp. 41-58). Association for Computational Linguistics. https://doi.org/10.18653/v1/2021.acl-long.4

    Sap, M., Card, D., Gabriel, S., Choi, Y., & Smith, N. A. (2019). The risk of racial bias in hate speech detection. In Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (pp. 1668-1678). Association for Computational Linguistics. https://doi.org/10.18653/v1/P19-1163

---

