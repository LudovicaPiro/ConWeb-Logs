# ConWeb-Logs
This source is a collection of conversation logs obtained using ConWeb. ConWeb is a browser extension that, is able to parse the content of a webpage and enable navigation through voice commands.

This source comprises conversation logs collected during user studies for the voice agent ConWeb. Two folders are present in this source: ConWeb V1.2 and ConWeb V2.0.

## ConWeb V1
The first version of the ConWeb NLU system was based on Rasa. To enhance its performance an NLU pipeline was designed to detect and overcome the errors of the Rasa model: The system would use the RASA model to perform intent and entity classification, if the confidence score was lower than a set treshold, the user utterance was sent to the **OpenAI interpreter** to classify intents and the entities. The OpenAI interpreter used the GPT 3.5 language model.



  ### Logs
  This logs in this folder were collected to assess the accuracy of the system and record the instances in which the RASA model failed and the OpenAI interpreter was invoked.
  The logs record utterances, intents, entities and whether RASA or GPT 3.5 were used for the classification.
  


## ConWeb V2.0
ConWeb V2 collects the tests made with the latest version of ConWeb. This version uses OpenAI GPT4o 
  ### Logs 
  This folder collects logs that record user utterances, intent, and entities. The files are separated based on the website used during the interaction. 
