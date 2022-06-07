# Unit13-Challenge
BOTS!
____


## You were hired as a digital transformation consultant by one of the most prominent retirement plan providers in the country; they want to increase their client portfolio, especially by engaging young people. Since machine learning and NLP are disrupting finance to improve customer experience, you decide to create a robo advisor that could be used by customers or potential new customers to get investment portfolio recommendations for retirement.
___


### main tasks 
___

- Define an Amazon Lex bot with a single intent that establishes a conversation about the requirements to suggest an investment portfolio for retirement.
- Make sure that your bot is working and responding accurately along with the conversation with the user, by building and testing it.
-  Create an Amazon Lambda function that validates the user's input and returns the investment portfolio recommendation. This task includes testing the Amazon Lambda function and making the integration with the bot.
_____
## inital Robo Advisor configuration 
* Created a Amazon Lex bot with an intent with corresponding slots.
* Created utterances that correspond with the created intent to generate dialog between user and Roboadvisor (sample utterances below)
    - I'm worried about my retirement
    - I want to invest for my retirement
    - I would like to invest for my retirement
* Created 3 basic slots to interact with user with the 4th slot being a custom slot to help user determine the recommend portofolio user desires
* 4th slot (custom slot)
    - congifured response cards for user to determine the recommened porfolio of user
    - ranging from low risk to very high risk
* Roboadvisor test (see screen recording)
____


### Enhance the Robo Advisor with an Amazon Lambda Function
____

- Create an Amazon Lambda function that will validate the data provided by the user on the Robo Advisor with parameters for validation
   - The age should be greater than zero and less than 65.
   - the investment_amount should be equal to or greater than 5000.

#### Investment Portfolio Recommendation
___
Once the intent is fulfilled, the bot should response with an investment recommendation based on the selected risk level as follows
   - none: "100% bonds (AGG), 0% equities (SPY)"

  - very low: 80% bonds (AGG), 20% equities (SPY)

  - low: 60% bonds (AGG), 40% equities (SPY)

  - medium: 40% bonds (AGG), 60% equities (SPY)

  - high: 20% bonds (AGG), 80% equities (SPY)

  - very high: 0% bonds (AGG), 100% equities (SPY)

After configuring Lambda, integrated the lambda function to Robo Advisor (_Amazon Lex_)
  - TEST TIME! 
