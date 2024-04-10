# ideation-tokenizer
Experiments on using AI for Ideation.

# Logit Bias
Some LLMs include the use of a logit bias to suppress token probability in output. On the flip side, you can also use logit bias to cause a token to show up more frequently. For ideation exercises, you can suppress certain tendencies that arise from the training data related to the "idea" [42877], "Idea" [40, 56188], "Ideas" [75344, 300], and "ideas" [94784] words. 

# GPT-3.5 and GPT-4 Tokenized Common Ideation Words
| Word/Phrase              | Token IDs            |
|--------------------------|----------------------|
| Personalized             | [35127, 1534]        |
| Virtual                  | [34126]              |
| Eco-friendly             | [36, 1030, 22658]    |
| AI-driven                | [15836, 32505]       |
| Mobile                   | [18876]              |
| Online                   | [20171]              |
| Sustainable              | [50, 42341]          |
| Customized               | [10480, 1534]        |
| subscription service     | [35504, 2532]        |
| Online tutoring platform | [20171, 78143, 5452] |

If you don't want these phrases in ideation output, here is the list:

logit_bias = {35127:-100,34126:-100,36:-100,15836:-100,18876:-100,20171:-100,50:-100,10480:-100,35504:-100,20171:-100,1534:-100,22658:-100,1030:-100,32505:-100,5452:-100,42341:-100,1534:-100,2532:-100,78143:-100}

This is all just for research and tinkering. 
