# Applied-Data-Science-Capstone
## Introduction
* The goal of this capstone is to predict if the Falcon 9 first stage will land successfully. 
* SpaceX advertises Falcon 9 rocket launches on its website, with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. 
* Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.
* As a Data Scientist working for a startup intending to compete with SpaceX, and I followed the Data Science methodology such as 
  1. Data collection
  2. Data wrangling
  3. Exploratory data analysis
  4. Data visualization
  5. Model development
  6. Model evaluation
  7. Reporting your results to stakeholders.
## Methodology
* Data was collected using SpaceX REST API and Beautiful Soup.
* Perform data wrangling
* Handled categorical variables, missing values and outliers.
* Perform exploratory data analysis (EDA) using visualization and SQL
* Perform interactive visual analytics using Folium and Plotly Dash
* Perform predictive analysis using classification models
* Built, Tuned, and Evaluated Decision Tree, KNN, Logistic Regression, and SVM models.
## Insights:
### Flight Number vs. Launch Site:
* Launch Site CCAFS SLC 40 had the most number of rocket launches.
* We can observe that as the Flight Number increases the success rate is also increasing but CCAFS SLC 40 does not show this pattern
  ![image](https://user-images.githubusercontent.com/48169929/226144635-a3212792-dd2d-41b5-b8ee-b6af49c46cef.png)

### Payload vs. Launch Site
* Most of the rockets launched in CCAFS SLC 40 had a Pay Load Mass(kg) of less than 8000.
* For Rockets with Payload mass greater than 10000 CCAFS SLC 40 has more success rate than KCS LC 39A.
* VAFB SLC 4E did not launch any rockets whose payload mass is greater than 10000.
* We can say that for higher payload mass the success rate is higher
  ![image](https://user-images.githubusercontent.com/48169929/226144652-a5fd9d0a-6c3d-456c-8e7f-e52293e740b1.png)
### Success Rate vs. Orbit Type
* Orbits such as SSO, HEO, GEO, and ES-L1 have a 100% success rate, while the SO orbit had a 0% success rate.
* However, further examination reveals that some of these orbits only have a single instance, such as GEO, SO, HEO, and ES-L1, meaning that more data is needed to discern patterns or trends before any conclusions can be drawn.
  ![image](https://user-images.githubusercontent.com/48169929/226144671-278e421f-69a9-4c9c-beca-30704e3daaec.png)
### Flight Number vs. Orbit Type
* Except for GTO and ISS orbit and the ones which have 2 or fewer data points, we can say that as the flight number is increasing the success rate is also increasing.
* For orbits such as GTO and ISS the success is fluctuating with the increase in Flight number.
  ![image](https://user-images.githubusercontent.com/48169929/226144692-1d440a53-4293-45e8-bc64-0574c77caedd.png)
## Model Comparision:
* Of all the models, Decision Tree has the best accuracy of 87.3 %
![image](https://user-images.githubusercontent.com/48169929/226144433-c66c4513-c786-487e-828d-767d2fc48e69.png)
## Best Model Evaluation:
![image](https://user-images.githubusercontent.com/48169929/226144491-5ad8cfd6-728e-4c6b-a094-4e103aa1f719.png)
## Conclusion:
* The Decision Tree Classifier model is the best Machine Learning approach for this dataset.
* The low-weight payloads (i.e., 4000kg and below) performed better than the heavy-weight payloads (i.e., above 4000kg).
* Starting from the year 2013 to 2020, the success rate for SpaceX launches is increased, with further R&D SpaceX can reach 100% success rate.
* KSC LC-39A has the most successful launches of any site a with success rate of 76.9%
* SSO orbit has the most success rate with a 100% success rate and more than 1 rocket launch.



