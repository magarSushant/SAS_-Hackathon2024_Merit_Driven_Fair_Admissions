# SAS Hackathon 2024: Fair and Ethical Admissions with Data-Driven Bias Mitigation

## Project Overview
This project focuses on addressing fairness in university admissions through **predictive modeling**. By leveraging tools like **SAS Viya and Python**, we aimed to create an **equitable admissions process** that reduces bias while maintaining predictive accuracy. The models were designed to balance **fairness and precision**, ensuring that admissions decisions are based on **merit** rather than any inherent biases in the data, which we uncovered through **exploratory analysis** and **bias assessments**.

## Objective and Approach
We aimed to build a predictive admissions model that enhances **diversity** by reducing **historical biases**, while maintaining **academic merit**. Our process included:
- **Conducting Exploratory Data Analysis** (with **Feature Engineering** and **Interactive Analysis**)
- **Building initial predictive models**
- **Using Bias Assessment tools** to identify performance and prediction bias
- **Rebuilding models** to mitigate historical biases
- **Evaluating trade-offs** between performance and fairness
- **Comparing results** of admissions predictions before and after bias adjustment

## Key Findings from EDA
- **Feature Engineering**: Variables like test scores, recommendations, and work experience were grouped for better insights. For example, applicants with 'High' test scores had a 52% admission rate, while 'Weak' scores had less than 1%.
- **Admission Disparities**: White applicants had a higher admission rate (14%) compared to Asian applicants (3.7%).
- **Legacy vs. Non-Legacy**: Legacy students were admitted at 48%, while non-legacy admissions were at 16%.
- **Bias Across Gender and Geography**.
- **Interactive Analysis**: Uncovered nuanced biases; for example, White applicants with high test scores and 3-5 years of experience had a 62% admission rate, compared to 20% for similarly qualified Asian applicants.

## Model Building and Skill Demonstration
We created two pipelines to explore both linear and non-linear approaches:
- **Pipeline 1**: Logistic Regression, Forest, Gradient Boosting
- **Pipeline 2**: SVM with RBF kernel, Neural Networks, Decision Trees. The **RBF kernel in SVM** was chosen due to its ability to handle non-linear relationships in the dataset.

We employed **automatic variable selection** in models like Logistic Regression, Neural Networks, and SVM to identify the most predictive features. This ensured we kept only the most relevant variables, improving interpretability and model performance. **The Forest model emerged as the best performer**, achieving an **accuracy of 88%** and a high **AUC (Area Under the Curve)** score, demonstrating its ability to handle complex relationships in the data.

## Bias Assessment: Performance Bias vs. Prediction Bias
- **Performance Bias**: For example, the model was more accurate for White applicants (True Positive Rate of 75%) than for Asian applicants (TPR 0%).
- **Prediction Bias**: For instance, the model predicted higher admission probabilities for White applicants by 30%, which was reduced to 8% after adjustments.

Bias was also observed in **country/region categories**, indicating disparities in predicted admissions based on applicants' geographic locations, notably between applicants from the **Americas vs. APAC regions**. By addressing these biases across multiple demographic factors—including **legacy status, gender, and geographic background**—the model's predictions became more equitable and balanced across diverse applicant groups.

## Trade-Off: Accuracy vs. Fairness
- **Accuracy dropped** from 88% to 81.3% after removing biased variables.
- **Fairness improved**, with representation for underrepresented groups increasing (e.g., Asian admissions rose from 12.5% to 45%).

In terms of **gender**, female admissions decreased post-adjustment, which may reflect merit-based differences rather than bias, as male applicants could possess higher merit indicators. **Universities may consider additional policies** to promote gender balance where needed, complementing this merit-focused approach.

## Future Considerations: Mission Statements, SOPs, and a Human Layer
In our model, Mission Statements and SOPs were excluded due to their subjective nature and missing data. However, future iterations could incorporate a **human layer** above model predictions, allowing for **qualitative assessments** of Mission Statements and SOPs. Admissions decisions shouldn’t rely solely on numerical predictions but should also consider applicants' **motivations and values**, where human insight plays a critical role. Enhancing this model with **behavioral and engagement assessments** could provide a more holistic view of each applicant.

## The Human Touch in Analytics
While data streamlines admissions decisions, combining **data-driven insights** with **personal evaluation**—such as reviewing Mission Statements and SOPs—ensures that each student’s unique journey is acknowledged, supporting a fair and inclusive admissions process.

## Technologies and Tools Used
- **SAS Viya**: SAS Visual Analytics, Bias assessment, predictive modeling
- **Python**: Data visualization, Interactive Analysis

## How to Use This Repository
Explore our **presentation video, slides, and downloadable presentation** for insights into how bias was mitigated through advanced analytics. Future improvements will integrate **additional data** like **soft skills and project-based assessments** to further enhance fairness.

- [Watch Presentation Video](https://drive.google.com/drive/folders/1FpPPq8cAnIIG8UZNMPeuzfLCrwDSxXae?usp=drive_link)
- [View PDF of Slides](https://github.com/magarSushant/SAS_-Hackathon2024_Merit_Driven_Fair_Admissions/blob/main/Ethical%20Admissions%20Model-Presentation%20Slides.pdf)
- [Download PowerPoint File](https://github.com/magarSushant/SAS_-Hackathon2024_Merit_Driven_Fair_Admissions/blob/main/Ethical%20Admissions%20Model-Presentation%20Slides.pptx)


## Conclusion
Our model offers a **data-driven approach to reducing bias** in admissions. While challenges like **gender disparity** remain, this project demonstrates the potential of **ethical AI** in building **fair, inclusive systems**.

## Disclaimer
The dataset used in this project was provided exclusively for the **SAS Hackathon 2024**. Due to data restrictions, it is unavailable in this repository.
