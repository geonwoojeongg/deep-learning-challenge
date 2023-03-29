# deep-learning-challenge

#Report

## OVERVIEW

The purpose of this analysis is to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

A CSV file contatining more than 34,000 organization information was given which was read into Pandas. The organizations received funding from Alphabet Soup. Additional metadata regarding the organizations have been given as well.

## Results

### Preprocessing
1. What variable(s) are the target(s) for your model?
The target variable wast the IS_SUCCESSFUL data (column), which signifies whether the funded money was used effectively. 

2. What variable(s) are the features for your model?
The measurable properties, namely features, include: 
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested

3. What variable(s) should be removed from the input data because they are neither targets nor features?
Variables EIN and NAME are removed from the input data because they are for identification purposes only.  


### Compiling, Training, and Evaluating the Model
4. How many neurons, layers, and activation functions did you select for your neural network model, and why?

For the first model I used two layers with 80 and 30 neurons, with 'relu' as the activation function. 

<img width="937" alt="Screenshot 2023-03-29 at 4 52 43 PM" src="https://user-images.githubusercontent.com/115575880/228665307-380b2628-3d4e-47d9-8271-e349b24b3526.png">

For the second model I used three layers with 80, 30, and 80 neurons, also with 'relu'. 

<img width="965" alt="Screenshot 2023-03-29 at 4 53 22 PM" src="https://user-images.githubusercontent.com/115575880/228665556-2dde0292-7840-4c80-9129-b401a2ee9947.png">

For the third model I used three layers with 120, 80, and 120 neurons, also with 'relu'. This time I increased the epoch number to 100.

<img width="963" alt="Screenshot 2023-03-29 at 4 53 36 PM" src="https://user-images.githubusercontent.com/115575880/228665687-b02b3358-522f-4b9d-9252-f162576cd3ec.png">

I started with 80 and 30 at the beginning to test how the initial accuracy rate would result in. It resulted like the following: 

<img width="825" alt="Screenshot 2023-03-29 at 4 58 50 PM" src="https://user-images.githubusercontent.com/115575880/228666173-0597a691-c918-4e9d-9da5-a9249c6677d0.png">

I thought the initial result of 0.728 accuracy was pretty close to the desired number (.75). So I decided to stick with 80 and 30 neurons but add another layer to increase the accuracy for the second attempt:

<img width="796" alt="Screenshot 2023-03-29 at 4 59 03 PM" src="https://user-images.githubusercontent.com/115575880/228666680-9e47b350-3eee-499d-9641-71169fc14511.png">

0.729 -- barely an increase.

For the third attempt, I decided to increase then neurons to 120, 80, 120 and the epoch to 100:

<img width="706" alt="Screenshot 2023-03-29 at 4 59 11 PM" src="https://user-images.githubusercontent.com/115575880/228667075-8a8146b2-0bf5-4377-adf2-a71b484e67cd.png">

0.727 -- another failed attempt at the target accuracy rate. I thought increasing the number of neurons would make the machine learn on a deeper, sophisticated level. However, it was not able to reach the desired number. 

5. Were you able to achieve the target model performance?

No. 

6. What steps did you take in your attempts to increase model performance?

As explained above, I tried increasing the number of layers, neurons, and epochs to increase accuracy. 


Summary: 

In conclusion, the results of the deep learning model has shown that in this particular dataset, increasing the number of layers, neurons, and epochs did not affect the machine in any positive direction. I recommend that trying different activation functions would be more effective in boosting accuracy. Also, dropping more columns on the dataset would be helpful in removing unnecessary information that only confuses the machine. 
