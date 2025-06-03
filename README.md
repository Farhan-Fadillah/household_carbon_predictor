# Household Carbon Predictor Machine Learning : A Small Step, Big Impact
As the global climate crisis intensifies, the need for collective action to reduce greenhouse gas emissions has never been more urgent. While governments and industries play a pivotal role in addressing environmental degradation, the impact of individual households is often underestimated. In reality, everyday activities such as energy consumption, transportation choices, and food habits at the household level significantly contribute to a country's overall carbon footprint.

![house](https://github.com/Farhan-Fadillah/picture_list/blob/df666f301915220c7d2273d31c5124cfd8eee6dc/household.jpg)

Despite growing awareness, many individuals remain unaware of the scale of their personal or household emissions, and more importantly, of actionable steps they can take to mitigate them. Existing tools and resources are often too generalized or technical, limiting their accessibility and relevance to the average household.

To bridge this gap, this project introduces a Machine Learning–based Household Carbon Predictor an intelligent system designed to estimate a household’s carbon footprint based on key lifestyle parameters. Beyond prediction, the system aims to educate users by providing personalized recommendations on how to effectively reduce their emissions. The tool serves both as a predictive engine and an awareness platform, empowering households to make data driven, environmentally responsible decisions.

# Project Significance and Benefits
1. Promotes Environmental Awareness at the Grassroots Level
   By offering personalized insights, the project helps individuals recognize the environmental impact of their daily choices, fostering a culture of accountability and sustainability.

2. Encourages Sustainable Behavior through Actionable Recommendations
   rather than simply presenting data, the system provides tailored suggestions such as energy saving practices, alternative transport methods, or dietary shifts that are feasible and impactful.

3. Bridges the Gap Between Data and Decision-Making
   Many households lack the tools to interpret complex environmental data. This project simplifies that process, enabling informed decision-making through user friendly interfaces and clear visualizations.

5. Scalable and Adaptable for Broader Impact
   While the focus is on individual households, the underlying model and framework can be adapted for community level or municipal use, supporting larger scale sustainability efforts.

6. Supports Climate Policy and Advocacy
   By collecting anonymized aggregate data, the system can also serve as a valuable resource for researchers and policymakers aiming to understand behavioral patterns and target interventions more effectively.

# Why This Project Matters
Tackling climate change requires both top down and bottom up strategies. This project addresses the often-overlooked bottom-up component by empowering individuals the smallest units of society to participate meaningfully in climate action. By leveraging machine learning to deliver personalized, actionable, and educational insights, the Household Carbon Predictor not only raises awareness but also inspires tangible change. In doing so, it contributes to a more sustainable and informed society, aligned with global environmental goals such as those outlined in the Paris Agreement and the United Nations Sustainable Development Goals (SDGs).

# Dataset Description

The Dataset consists of four columns:
1. electricity_kwh = Monthly electricity consumption (kWh)
2. gas_m3 = Monthly gas consumption (cubic meters)
3. transport_km = Monthly transportation distance traveled (km)
4. carbon_kg = Monthly carbon emissions in kilograms (target)

Notes:
•	The first three columns are input features representing household energy and transport usage.
•	The last column, carbon_kg, is the target variable representing the carbon footprint to be predicted.

This dataset captures key household activities that contribute to carbon emissions, making it suitable for modeling carbon footprint prediction.

# Machine Learning Model: Linear Regression

Why Linear Regression?
   1. Simplicity & Interpretability: Linear regression is straightforward and provides clear insight into how each feature (electricity, gas, transport) contributes to carbon emissions.
   2. Suitability for Continuous Target: Since carbon emissions are continuous numeric values, linear regression is a natural choice.
   3. Good Baseline Model: It serves as a strong baseline to understand relationships before exploring more complex models.
   4. Efficiency: It trains quickly and requires less computational resources, ideal for your project scope.

![linier](https://github.com/Farhan-Fadillah/picture_list/blob/e765fc92f2375b9199f5b859e692510854e4db9a/linier%20regress.png)

How the Model Works?
The model learns coefficients (weights) for each input feature to best fit the target carbon emissions. It minimizes the difference between predicted and actual carbon emissions using the least squares method. The model's performance is evaluated using the R² score, which measures how well the model explains the variance in the data

# Project Flow Overview
Step-by-step Flow
   1.	Data Input: User inputs monthly household data: electricity consumption (kWh), gas consumption (m³), and transport distance (km).
   2.	Model Training:
      •	The dataset is split into training and testing sets (80% train, 20% test).
     	•	Linear regression model is trained on the training data.
     	•	Model performance is evaluated on the test set using R² score.
     	•	The trained model is saved to disk for reuse.
   3. Prediction:
      When the user inputs new data, the saved model is loaded. The model predicts the estimated carbon emissions based on the input features.
   4. Streamlit App Interface:
      - User-friendly web app for inputting data and viewing results.
      - Displays predicted carbon emissions.
      - Visualizes comparison between user emissions and average national emissions.
      - Provides personalized environmental recommendations if emissions exceed certain thresholds.
   5. Recommendations System:
      - If electricity consumption > 300 kWh, suggests reducing electricity use.
      - If gas consumption > 40 m³, suggests better home insulation or alternative cooking methods.
      - If transport distance > 250 km, suggests using public transport or carpooling.
      - If none of these thresholds are exceeded, encourages maintaining current eco-friendly habits.

# Streamlit App Features
Features:
1. Input Fields = Number inputs for electricity, gas, and transport consumption.
2. Carbon Emission Prediction	= Displays predicted carbon emissions in kg CO₂ per month.
3. Visualization = Bar chart comparing user emissions with average national emissions.
4. Environmental Tips = Dynamic recommendations based on user input to encourage greener habits.
5. Model Training & Loading = Automatically trains the model if not found, then loads the saved model for predictions.
6. User Interface	= Clean, intuitive layout with titles, captions, and success/info messages for user feedback.

![household_app](https://github.com/Farhan-Fadillah/picture_list/blob/a42aece13c0df38680f843492837e4fde63e7ab8/household%20app.png)

![household_app_result](https://github.com/Farhan-Fadillah/picture_list/blob/a42aece13c0df38680f843492837e4fde63e7ab8/household%20app%20result.png)

# Flow Diagram 
![flow_household](https://github.com/Farhan-Fadillah/picture_list/blob/55704f385501af586583832255d4a0204062bdae/FLOW%20HOUSEHOLD%20ML.png)

# Summary
The project effectively combines a simple yet powerful linear regression model with an interactive Streamlit app to predict household carbon emissions. The dataset features are well-chosen to represent key emission sources, and the model choice balances accuracy with interpretability. The app enhances user engagement by visualizing results and providing actionable recommendations, encouraging sustainable behavior.

# Application Link
[Click Here](https://household-carbon-predictor.streamlit.app)








