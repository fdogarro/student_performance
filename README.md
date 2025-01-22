## Factors Influencing Student Exam Performance: Multi-Model Analysis

### Felicia D. O'Garro

### Executive Summary

Understanding the factors that influence student performance is critical for designing effective interventions to improve academic outcomes. Factors such as study habits, parental involvement, attendance, prior achievement, access to tutoring, and parental education levels all contribute to academic success, but their relative importance and interactions remain unclear. This study aims to address this gap by investigating the drivers of exam scores using a dataset of 6,607 records and 20 features, including exam scores, attendance, study habits, and parental involvement.

This research employs a comprehensive methodology to uncover patterns and relationships in the data. Correlation analysis, heatmaps and other visualizations will identify initial relationships among variables. Regression models will quantify the combined effects of predictors, such as hours studied, attendance, and parental involvement, on exam scores. Bayesian models will integrate prior knowledge, such as the relationship between exam scores and previous performance, to refine predictions. Poisson models will provide insights into count data, such as tutoring sessions. Through these techniques, we aim to identify the most significant predictors and understand the interactions among them.

The findings from this research are expected to provide actionable insights. Key insights include the relationship between study time, attendance, and exam scores; the impact of parental involvement and education on student success; and the role of academic resources, such as tutoring, in improving performance. These results will guide the design of targeted interventions, enabling more equitable learning opportunities and resource allocation.

By using a multi-faceted analytical approach, this research seeks to answer critical questions about the drivers of student success, providing a robust foundation for improving academic outcomes in diverse educational settings.


### Modeling The Response Variable

To model the response variable (exam scores), a multi-faceted approach combining several statistical techniques will be employed. Initially, Ordinary Least Squares (OLS) regression will explore the relationship between exam performance and various predictors, including hours studied, previous scores, parental involvement, parental education level, tutoring sessions, and attendance.

Exploratory data analysis (EDA) will help visualize relationships and identify potential interactions between variables, using plots to uncover patterns and outliers. The assumptions of OLS regression, such as linearity, normality of residuals, homoscedasticity (constant variance of errors), and multicollinearity, will be assessed. If heteroscedasticity (non-constant variance) is detected, transformations or robust regression techniques will be considered.

In addition to OLS, Logistic Regression will model binary outcomes, such as pass or fail classifications based on exam scores. This method predicts probabilities and identifies key predictors influencing the likelihood of passing. Model performance will be evaluated using metrics like accuracy, precision, recall, and F1-score, alongside cross-validation to ensure generalizability. Visualizations, such as histograms of predicted probabilities and plots of predictor relationships, will aid interpretation and refinement.

Bayesian models will be explored to incorporate prior knowledge, such as the relationship between exam scores and previous academic performance. These models provide a probabilistic framework to handle uncertainty and leverage prior distributions for robust parameter estimates. Posterior distributions will offer insights into the most likely parameter values and their credible intervals, allowing for a nuanced understanding of predictor impacts, particularly when sample sizes are small or variability is high.

Building on this, Hierarchical Bayesian models will account for group-level effects, such as differences in exam performance across parental education levels. These models capture both population-level effects and group-specific deviations, offering a comprehensive view of how predictors affect exam scores across different groups. This structure is particularly valuable for understanding nested or hierarchical data while quantifying uncertainty at multiple levels.

For count data, such as the number of days attended, Poisson regression will analyze its influence on exam scores. This technique is ideal for non-negative count variables that follow a Poisson distribution. If overdispersion (variance exceeding the mean) is detected, alternative models like Negative Binomial regression will be considered. Visualizations, including predicted attendance versus predictors and residual plots, will evaluate model fit and guide refinements.

Model validation and residual analysis will ensure the robustness and reliability of findings. Cross-validation and residual diagnostics will help identify patterns or deviations from model assumptions. By integrating these techniques, the goal is to identify the most influential predictors of exam performance, understand their interactions, and develop a reliable predictive model for student outcomes.

### Conclusion

The analysis revealed critical insights into the factors influencing student exam performance by leveraging multiple modeling approaches, including OLS regression, Logistic Regression, Bayesian methods, Hierarchical Bayesian modeling, and Poisson regression. Each method offered unique perspectives, comprehensively understanding the relationships between predictors and outcomes. The comprehensive model (Model 1) performed best among the OLS models, explaining 62.6% of the variability in Exam_Score. It highlighted the significant contributions of family-related predictors such as Parental_Involvement and Parental_Education_Level, emphasizing the importance of external support alongside academic effort. However, diagnostic issues like heteroscedasticity and non-normality of residuals suggest further refinement of these models.

The Logistic Regression model excelled at predicting binary outcomes, achieving an accuracy of 87.4%. Predictors such as Tutoring_Sessions, Hours_Studied, and Attendance significantly influenced pass/fail outcomes, with tutoring having the most substantial impact. The model’s consistent cross-validation performance and clear visual separation between predicted probabilities for pass and fail outcomes instill confidence in its reliability. Bayesian regression further complemented these insights by providing probabilistic estimates, with Attendance emerging as the strongest predictor. Its narrow, credible intervals and strong convergence metrics underscore the robustness of the estimates, making it a valuable tool for noisy or limited data scenarios.

The Hierarchical Bayesian model offered a nuanced view of group-level and population-level effects, revealing that Parental_Involvement is the most significant predictor across groups. However, group-level variations were minimal, and convergence issues for some parameters weakened confidence in group-specific estimates. Finally, the Poisson regression model struggled to explain variability in Attendance due to overdispersion in the data, indicating that a Negative Binomial model would be more appropriate for count-based outcomes like Attendance.

Refining the models is essential to address diagnostic issues, particularly for OLS and Poisson regression. Incorporating additional predictors, exploring interaction terms, and considering longitudinal approaches could further enhance the analysis. The Logistic Regression and Bayesian models can be reliable tools for predicting student outcomes and identifying at-risk students, guiding targeted interventions such as increased tutoring or attendance monitoring. Moreover, insights from the Hierarchical Bayesian model can inform broad and localized educational policies, focusing on enhancing parental involvement and improving study habits. These findings provide a robust foundation for actionable strategies and future research to optimize student success.
