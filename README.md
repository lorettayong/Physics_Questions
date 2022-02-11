# Introduction

This second project was developed to fulfil the Data Science module requirements of IBM's i.am-vitalize programme. The group had a teammate who is a Subject Matter Expert (SME) in the education field of Physics taught at the [Junior College levels in Singapore.](https://en.wikipedia.org/wiki/Junior_college#Singapore). We therefore collectively felt that it would be an interesting experience to do the project with an SME within our midst.

While we heavily relied on the key principles of Enterprise Design Thinking (EDT) to ensure all group members converged back when we digressed away too much, all five stages of the Data Science lifecycle (i.e Planning Analytics, Descriptive Analytics, Diagnostic Analytics, Predictive Analytics and Prescriptive Analytics) formed the main backbone of the project structure.

We approached this project by keeping the EDT framework in mind, which helped us to identify the pain points faced by Physics educators and complete the Planning Analytics portion. Additionally, we spent a considerable amount of time to understand the business case in a much more in-depth manner. I had volunteered to take responsibility for the Predictive Analytics, working hand in hand with a project mate who was taking charge of the Prescriptive Analytics. This was arranged as we felt that the last two stage were strongly associated with each other.

Similarly, I only had one mission in mind for the presentation of my scope: to be able to effectively communicate how the team had built the machine learning model, selected the most optimised pipeline and interpreted the results upon model deployment in relation to our dataset. Our project team's slides deck is available in this repository for your reading pleasure.

My presentation content comprised of the following:

*We have used IBM Watson Studio’s AutoAI toolkit to conduct our team’s predictive analytics. The toolkit has massaged our data to automatically select the best algorithm and determine the best model with optimised hyperparameters. In the context of our business case, as we are interested in predicting how difficult a specific exam question is, so as to help our end users, who are educators, objectively determine the quality of the exam questions that they curated, we have selected the p-value as our target variable. Let us now look at how AutoAI has identified the most suitable model for our business case.*

*Upon reading the dataset that we have fed into the AutoAI experiment, the toolkit automatically split our data into training and holdout data based on a ratio of 9:1. Preprocessing was done, followed by the selection of the top two most suitable machine learning algorithms applicable to our data. Here, we can see that the two algorithms that have been determined to best match our data and prediction type are linear regression and ridge regression.*

*Afterwhich, through the application of intelligent automation by AutoAI, feature transformation capabilities were applied to the model pipelines so as to generate different variations of machine learning models. From the progress map, we can see that there were two main transformers adopted by AutoAI. They are hyperparameter optimisation, which refines and optimises the model pipelines using model training and scoring, and feature engineering, which transforms the raw data into combinations of features that best represent the problem to achieve the most accurate prediction. We will now look at how the pipelines were ranked based on their optimal performance levels.*

*Based on the pipeline leaderboard, we can see that Pipeline 3 has been identified to be the best performing model pipeline, which is linear regression with further enhancements using hyperparameter optimisation and feature engineering. Even though the top 4 ranked pipelines attained the same RMSE, or Root Mean Square Error, value of 0.163, we have decided to select Pipeline 3 for our model deployment.*

*In addition, while considering which pipeline was most suitable for our business case, upon  meticulously studying our dataset and going through numerous rounds of AutoAI experiment iterations, we were convinced that linear regression is indeed the most basic model to start with. We were aware that the data most relevant to addressing our target users’ pain points are predominantly numerical values, and these values are linearly related to one another, so the type of regression algorithm applicable to our business case would be multiple linear regression. We then moved on to investigate the model’s behaviour in respect to our dataset.*

*On the left, we have the feature summary of the top performing pipeline, Pipeline 3, which identified the Physics topics, or features, and the respective levels of significance they played in constructing the machine learning model. We could see that the model had checked every feature found in our data and determined how much each feature had affected the final outcome.*

*In order to better visualise how the model behaved, we compared this with the equation used for multiple linear regression algorithm as shown below. The model first saw the manner that these features changed, produced the regression coefficient values respectively as per the equation below, which we have circled in pink here, and performed a summation based on the number of times that the features were appearing so as to obtain the predicted value.*

*While we may not be able to see how this is actually happening since the machine learning model is the blackest of all black boxes, we could gain a rough idea on what the model was trying to do and better appreciate this feature summary. It had identified only relevant features with numeric values that were appropriate for the algorithm and used them to predict the value of Y, or our target variable of p-value, such that the error difference between the predicted value and the true value stayed minimal, thereby achieving the best fit regression line in relation to our data.*

*Fascinatingly, the model had also recognised the top five ranked Physics topics to have high correlation to the p-value. These same features would be used as our basis for the validation of our data model. We will be exploring the test results next.*

*And on the right, we have highlighted, in pink arrows, the two most important metrics we have used to assess the performance of our model. Pipeline 3, which gives the cross validation scores of 0.163 and 0.218 for the RMSE and R squared measures respectively, tells us that the model has performed relatively well. In consideration that our dataset is restrictive since the data comes from a single junior college of very similar competency levels of students, we could conclude that the model’s performance is satisfactory.*

*Upon deployment of our selected model in Watson Studio, we tested the prediction from the user interface that the platform provides. The testing was done based on the features that were found to play higher significant roles in the model’s algorithm. They are Superposition, EMI or Electromagnetic Induction in short, EM or Electromagnetism in short, Dynamics and Gravitation. In order to determine the prediction accuracy of our model, we kept a simple rule of thumb in mind: the higher the level of difficulty, the lower the p-value, the better the quality of the exam question.*

*We decided to only select exam questions from the five features, or Physics topics, as mentioned earlier. For the purpose of testing the accuracy of the model, we chose exam questions that had values which reflected high difficulty levels and small p-values as ascertained by our subject matter experts. A screenshot of the results from the model validation exercise that we did is as shown on the bottom left of this slide. We have reproduced them on the right along with the values from our dataset as a means of comparison.*

*Interestingly, we observed that with reference to the table of p-value threshold ranges, the p-values of exam questions for Superposition, EMI, EM and Dynamics were predicted to lie within the moderate difficulty level range. We are therefore able to conclude that the machine learning model could give a more objective prediction of how difficult an exam question is.*

Thank you for taking the time to read about my team's data science project.