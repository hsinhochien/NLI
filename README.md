# Argument Mining Analysis
Given two sentences, the task is a three-class classification problem:
* Class 0: There is no detected relation between the two sentences.
* Class 1: There is a “Support” relation from sentence 1 to sentence 2.
* Class 2: There is an “Attack” relation from sentence 1 to sentence 2. 

Data example: <br>
\[ <br>
"Some have a 24-month clock, and there are even some that have a 30-month clock.", <br>
"They come back in and they pay less for the service but they pay more for their smartphone.“, <br>
0 <br>
], <br>
\[ <br>
"Japan as a geography for us is a high transactional market.", <br>
"The improvement in that in Q3 is obviously very high margin and also the bottom.", <br>
1 <br>
] <br>

### LLM.ipynb 
This file primarily calls Gemini to classify the given text and tests whether different prompts yield different results. <br>
(API key needs to be filled in.) <br>
Prerequisites:
* Python 3.10
* ```pip install tqdm google-generativeai```
    
### LM.ipynb
This file first uses a pre-trained model for direct prediction (without fine-tuning), and then performs prediction after fine-tuning the pre-trained model. <br>
Prerequisites:
* Python 3.10
* ```pip install torch transformers```
