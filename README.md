# chatbot_dialogflow

## Overview
I developed a chatbot using a platform called dialogflow developed by google and used an API which translate the message you asked to this chatbot. Also, I used an API which enable the chatbot to reply us the weather forecast if you ask the chatbot with time and the location that you need the weather forecast from. I used the fulfillment from [here](https://github.com/juanantoniofm12/fulfillment-webhook-translate-python) for the translate API and the fulfillment from [here](https://github.com/dialogflow/fulfillment-weather-python) for weather foecast API.


## Instruction (ex. weather forecast)
Dialogflow has an `Intents` item, an `Entity` item, and many other items. You can set keywords in `Entity` and decide how to respond or how to react to the user's words in Intents. In addition, `Fulfillment` in Dialogflow allows you to call information from outside.

In this case, I want to call up weather information, so I chosoe programming code using the Python from Github and entered it into Fulfillment's webhook via Heroku.
1. Go to [Heroku](https://www.heroku.com/)
2. choose repository of [weather forecast](https://github.com/dialogflow/fulfillment-weather-python)
3. click `deploy to Heroku` -> `Your app was successfully deployed`

Next, setup your [Dialogflow](https://cloud.google.com/dialogflow)
1. Open Fullfillment in Dialogflow and turn on `ENABLE` for Webhook to allow Webhook changes.
2. Insert Fulfillment URL as follows (put your own `App Name`)
3. `https://[App Name].herokuapp.com/webhook`
4. Set Intents. Enter "weather for [city]" as Training Phrases, and "PARAMETER NAME," "ENTITY," and "VALUE" will automatically be written in response to the city name.
5. Enter "yahooWeatherForecast" as the "Action". The reason for this is that it is set to work when "Action=yahooWeatherForecast", as you can see from the programming code retrieved from Github.
6. Allow the Fulfillment call at the bottom of Intents and you are done.


Fianally, setup demo mode,
1. click `intergrations` in Dialogflow
2. Turn on `Web Demo`. Then click `SETTING`
3. click the link and move to the demo page
4. By using the code under that link, you can easily put it on your website, etc. 


## What is Dialogflow
Dialogflow is a natural language understanding (NLU) platform developed by Google. It allows developers to build conversational interfaces, such as chatbots and virtual assistants, that can understand and respond to user inputs in a human-like manner. Dialogflow uses advanced machine learning algorithms and natural language processing (NLP) techniques to interpret user queries and generate appropriate responses.

## What is Fuilfillment
Fulfillment, in the context of chatbots and virtual assistants, refers to the process of generating and delivering a response to a user's query or request. When a user interacts with a chatbot or virtual assistant, the system needs to interpret the user's input, determine the appropriate response, and deliver it back to the user.



[API](https://github.com/juanantoniofm12/fulfillment-webhook-translate-python)
[API](https://github.com/dialogflow/fulfillment-weather-python)

(08/03/2018)
- [demo](https://console.dialogflow.com/api-client/demo/embedded/5ef0a2c6-38cf-407c-9423-ec3a0c208f18)
- [image](https://github.com/tinaba96/chatbot_dialogflow/assets/57109730/c6fe811a-b6cf-42f1-a424-18b7f0d66dba)

