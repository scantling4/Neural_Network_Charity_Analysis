# Neural_Network_Charity_Analysis

## Overview 
Alphabet Soup is a nonprofit foundation that has donated over 10 billion dollars over the past twenty years to various organizations. The purpose of this analysis is to create a binary classifier neural network to decide which companies that Alphabet Soup should invest in and which ones are too high risk. The ultimate goal is to create a data-driven solution to make these predictions with consistent accuracy. 

### Tools
- TensorFlow 
- skikitlearn
- Python/Pandas

## Results 

### Data Preprocessing 
The target variable for this analysis is the "IS_SUCCESSFUL" column which is coded in 0's and 1's and shows if a particular nonprofit utilized their money effectively. The "EIN" and "NAME" columns were removed because they have no bearing on the target variable. The rest of the columns became features for the model. 

### Compiling, Training, and Evaluating the Model 
The first model that I created had 12 neurons in the first layer and 6 in the second layer. Both of the layers had relu activation functions and the output layer had a sigmoid activation function. I initially began with these parameters because reul handles nonlinear data better. I chose to have two layers because the second layer allows the inputs from the first layer to be reweighted. 
Performance metrics from my first model: 
![model 1](/model_1.png)

In the second model that I created, the first modification was the removal of the "SPECIAL_CONSIDERATIONS" column. This seemed like a logical step to take because the data may have confused the model. I lowered the threshold for the classification column so that there were more unique values from that column. In addition to these two modifications, I added a third layer with 6 neurons. I wanted to see if any additional re-weighting would affect the accuracy. 
Performance metrics from this model: 
![model 1](/model_2.png)
In the third model, I decided to go back to the initial threshold for the classification column. I decided to change the activation function to tanh for the three layers to see if the model would perform any better. 
Performance metrics from this model: 
![model 1](/model_3.png)
In the fourth model, I decided to remove the "STATUS" column for the same reason I removed the "SPECIAL_CONSIDERATIONS" column: it might be confusing for the model. I also changed the activations back from tanh to relu. I then changed the neurons in the first layer to 12 and the second layer to 8.
Perormance metrics from this model:
![model 1](/model_4.png)

## Summary 
Despite making multiple modifications to my model, I was not able to achieve a 75% accuracy rating. This could have been because I did not use the correct activation functions or combination of activation functions. It also could have been because I did not have the right amount of layer or neurons within each layer. Next time, I would do more research into what is the recommended amount of neurons and layers for the data I was working with. I also may consult with other team members or see if there are any additional resources online that I could reach out to. I would also look into what activation functions are recommended for the specific data I am working with. 
