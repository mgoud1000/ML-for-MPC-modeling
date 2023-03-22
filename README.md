# ML-for-MPC-modeling
Project Proposal
Domain
A sophisticated form of process control called model predictive control (MPC) is used to manage a process while adhering to a set of restrictions. (1)Since the 1980s, it has been utilized in chemical and oil refineries as well as process industries. (2)It has recently been employed in power electronics, models for balancing power systems and automotive industry(3). Model predictive controllers rely on dynamic processes models, most frequently linear empirical models acquired by system identification. The fundamental benefit of MPC is that it enables timeslot optimization while taking future timeslots into consideration. MPC is also capable of foreseeing future events and taking appropriate management measures. This prediction capability is not present in PID controllers.(4)

 
Figure.‎0.1 general MPC configueration
Problem statement
Control is one of several sectors where machine learning has lately become successful and gained popularity. Machine learning is a set of techniques for extracting mathematical models from data. (5)
Machine Learning (ML) can be used to resolve the following problems in the field of MPC:
How can one create accurate prediction models from data?
How can I choose the ideal MPC parameters?
Can the problem be made smaller?
How do you warm up the solver?
Solution statement
In this project we will try to address the first problem where several models will be built and their accuracy for prediction will be tested against real data obtained from step testing for fractionator plant where manipulated variables of the system are changed to estimate and the changed in the controlled variables of the system are measured. By stabilizing operation, boosting throughput, enhancing fractionator performance, lowering product quality loss, and lowering utility consumption, model-predictive control (MPC) enhances the capability of process units. 
Furthermore, higher-level applications like planning models and process optimizers can use real-time data from MPC. 
The distributed control system (DCS), advanced regulatory controllers (ARCs), and laboratory data are the sources of input for the MPC. A well-designed MPC controller moves several variables simultaneously once every minute, or even more often in some circumstances, in response to any disturbance variables present to the system like changes in feedstock, ambient temperature, and other factors.













Datasets and Inputs:
The data set are obtained from areal fractionator tower real data of step testing used to implement MPC control scheme to the plant where the fractions of (Propane (C3H8), Pentane (C5H12) and Heptane (C7H16)) are separated.
Number of samples=5820 Number of variables (Tags)=18 Sample period=60 sec.
Time range for the dataset:
From: 10/01/2009 8:14:00   To:10/05/2009 9:13:00
Benchmark Model
The Benchmark model that is used is linear regression model.



Evaluation Metrics
Since we are dealing with nonlinear regression model several metrics will be used to determine the accuracy of our model where each metric has ups and downs:
RMSE: 
Root Mean Squared Error (This is just the square root of the MSE.) eliminating MSE from choice as it more superior and related to the standard deviation of the error term; easy to calculate; in the same units of yet the relationship to standard deviation can range from unhelpful to downright misleading if the error is not Gaussian or does not have a constant standard deviation.
R2:
Although R2 is related to comparing your predictions to the predictions of a baseline model yet it has poorly performance when it comes to nonlinear models and lacks its usual "proportion of variance explained" interpretation.
MAPE: Mean Absolute Percentage Error
Handles data on different scales but overestimates and underestimates are not penalized equally.
Project Design
In this project I will first look at the data to determine what shape and format they are in before I even begin training models. To understand the data distribution better, we will visualize some graphs.
Remove bad data from our dataset for data cleaning and preparation and use PCA to determine the required features and perform feature engineering on the data.
Then we start training the benchmark model for linear regression then several models will be trained like (ensembled models (bagging and trees) and neural network models.
The models will be tested to check for the best performance and accuracy.
Reference
1. 	Cutler and Ramaker. 1980_Cutler-Ramaker_Dynamic-matrix-control_JACC1980. 1980. 
2. 	Richalet J, Rault A, Testud JL, Papon J. Model predictive heuristic control. Applications to industrial processes. Automatica. 1978;14(5):413–28. 
3. 	Schwenzer M, Ay M, Bergs T, Abel D. Review on model predictive control: an engineering perspective. Int J Adv Manuf Technol. 2021;117(5–6):1327–49. 
4. 	Bemporad A. Machine Learning Methods for Model Predictive Control. Slide. 2021; 
5. 	Jain A, Morari M, Pappas GJ. Methods for Data-driven Model Predictive Control. ProQuest Diss Theses [Internet]. 2020;104. Available from: https://www.proquest.com/dissertations-theses/methods-data-driven-model-predictive-control/docview/2446708156/se-2?accountid=15179%0Ahttps://media.proquest.com/media/hms/PFT/2/jhrDH?_a=ChgyMDIyMTIxOTA3MDU1MDY4MDo1NDI5MDASBTk0MzI4GgpPTkVfU0VBUkNIIg4xNjUuMT

