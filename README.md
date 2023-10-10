## Airbnb Rental Price Prediction
## read me
The primary objective of this report is to conduct a comprehensive analysis of the Sydney Airbnb rental dataset, with a focus on identifying the most impactful features. This dataset has been divided into two sets: a training dataset comprising 12,941 rows and 61 columns and a test dataset containing 5,547 rows. Given the dataset's size and complexity, I have categorized it into three distinct groups: host & host listings, property, and review data. This categorization streamlines my data analysis process, making it more efficient.

My research is centered around the variable 'price.' An initial examination of the dataset revealed that the relationship between price and its frequency follows a right-skewed distribution, with a significant concentration of rental prices falling within the range of 0 to 1000. To improve model performance and better fit the data, I have employed a standardization technique, transforming the price variable into a logarithmic form.

Upon reviewing the dataset, I have selected the following models for analysis: Ordinary Least Squares (OLS), Ridge regression, Lasso regression, XGBoost, and Random Forest. Linear regression serves as my benchmark model due to its low computational cost and interpretability. As my goal is to identify the top three influential factors affecting price, a well-trained linear regression model allows for straightforward interpretation, aiding in the selection of the most significant features. However, it's important to note that OLS-based linear regression models can be prone to overfitting. To mitigate this issue, I have incorporated Ridge and Lasso regression techniques, both of which employ regularization to prevent overfitting. Additionally, I have included two tree-based models: XGBoost, which utilizes regularization hyperparameters to control pruning, and Random Forest, known for its robustness against outliers. While Random Forest may not always yield the highest accuracy, it is effective in preventing potential misdirection caused by outliers.

To ensure accurate and meaningful insights from this dataset, I have not only categorized the data but also visualized predictor values with various features to gain a statistical understanding. Following data preprocessing, I have selected five models, each offering unique advantages for cross-validation and result comparison. To determine the three most impactful factors, I have evaluated these five models using Root Mean Square Logarithmic Error (RMSLE). Finally, I have applied model stacking to combine the top-performing models, ensuring a more unbiased and robust conclusion.

## Conclusion
High-priced properties exhibit a distinct pattern on the graph, tending to cluster more densely on the eastern and southern sides. This phenomenon is likely influenced by Sydney's unique geographical characteristics. With the coastline stretching along the eastern and southern directions, properties in these areas often offer picturesque ocean or harbor views. Additionally, the iconic Sydney Opera House is situated in this part of the city, further enhancing its appeal.

Different suburbs in Sydney boast a diverse range of amenities. As revealed in the neighborhood frequency graph in future analyses, the top seven frequently searched suburbs include Sydney, Waverley, Randwick, Manly, Warringah, North Sydney, and Woollahra. Convenient transportation is a top priority for tourists, making Sydney's central business district, in particular, a popular choice.

However, it's important to note that a few outliers significantly exceed the typical price range, as evident in the room type and price boxplot diagram. These variations may be attributed to various property-specific metrics, such as the style of decor, the number of reviews for the host on the platform, or overall review trends. Even when two properties share similar locations, superior decor quality can lead to higher rental rates. In the long term, substantial investments in renovations often yield higher rental returns, as supported by Think Architecture (2019).

Furthermore, hosts managing multiple properties tend to receive more reviews, leading to the establishment of professional Airbnb property management companies. This trend has been further exacerbated by the pandemic that began in 2019. The platform has also responded to the special situation, as evidenced by the launch of a new COVID-19 support package in Australia (Finder, 2022). Consequently, increased demand has driven up prices for private properties.
## Results
Key factors influencing house prices on Airbnb have been identified through the analysis: location, accommodation capacity, and amenities. In particular, the impact of "accommodates" is the most substantial, as indicated by a correlation coefficient of 0.64, revealing that higher prices tend to be commanded by larger properties. To enhance customer loyalty, a focus can be placed on the delivery of high-quality services, adaptability to changing circumstances, and the facilitation of effective communication, as suggested by Lee and Deale (2021). The implementation of this strategy can lead to profitability and customer loyalty for Airbnb, especially in a post-pandemic context.

## Methodology
An outline is provided for the approach taken in predicting Airbnb's home rental prices using various machine-learning models. The objective is to determine the best-performing model for this task. The model selection encompasses Ordinary Least Squares (OLS), Ridge, Lasso, Random Forest, and XGBoost. To establish a baseline for comparison, a straightforward yet effective method—multi-linear regression—is also employed.

To evaluate the performance of the models, Root Mean Square Logarithmic Error (RMSLE) is utilized. This metric places a greater emphasis on the penalty associated with underestimating true values, a consideration of greater significance in a business context than overestimation.

## Model Performance
The RMSLE results for our models are presented in the following table, with the lowest error achieved by XGBoost:

Model	XGBoost	Random Forest	Ridge	OLS	Lasso
RMSLE	0.386	0.389	0.410	0.410	0.410
The prediction process entails the importation of the necessary libraries, the execution of the train-test split, and the generation of final predictions using the test dataset. Subsequently, the model's output is submitted to Kaggle for the acquisition of validation scores.







