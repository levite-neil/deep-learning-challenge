# deep-learning-challenge

The purpose of this analysis was to determine wheater applicants submitted to the nonprofit foundation Alphbet Soup for funding  had a good chance for succeess in their ventures. We were presented with 34,000 organziations that were already funded by Alphbet Soup over the years that had effectively use the funds and those that didn't.

* Data Preprocessing
    ## Target:
    *IS_SUCCESSFUL—Was the money used effectively

    ## Features:
    *APPLICATION_TYPE—Alphabet Soup application type
    *AFFILIATION—Affiliated sector of industry
    *CLASSIFICATION—Government organization classification
    *USE_CASE—Use case for funding
    *ORGANIZATION—Organization type
    *STATUS—Active status
    *INCOME_AMT—Income classification
    *SPECIAL_CONSIDERATIONS—Special considerations for application
    *ASK_AMT—Funding amount requested

    ## Removed variables:
    *EIN-Identification
    *NAME—Identification

*Compiling, Training, and Evaluating the Model
    For the first attempt, I used 80 neuron in the first layer and 30 in the second layer. I used relu for my activation.For my second attempt, I used the following:
    *Layer 1 80 neurons with the relu activation.
    *Layer 2 30 neurons with the relu activation.
    *Layer 3 20 neurons with the relu activation. 
    *Layer 4 20 neurons with the leaky_relu activation. 
    *Output layer 1 with 1 neuron and sigmoid activation.
    
    I was not able to achive the target model performance of 75%.
    To increase the models performance, I removed EIN, NAME, and AFFILIATION columns, added more APPLICATION_TYPEs and CLASSIFICATION to the Other bin accordingly.


The summerized results for my deep learning model:

268/268 - 0s - loss: 0.6143 - accuracy: 0.6567 - 500ms/epoch - 2ms/step
Loss: 0.6142776012420654, Accuracy: 0.6566764116287231

Summary: A model with more neurons and fewer layers could improve this clssificaiton problem. Also, binning fewer Applications Type and Classification to Other. We could use hyperparameter tunning as it would adjust the neurons, layers, and activations automatically according to the hyperparameter tunning to try and improve the prediciton. Hyperparameter tunning would prevent over-fitting and under-fitting of the data.