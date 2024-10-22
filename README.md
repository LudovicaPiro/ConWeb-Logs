# ConWeb-Logs
This source is a collection of conversation logs obtained using ConWeb, a browser extension that enables conversational web browsing

This source comprises conversation logs collected during user studies for the voice agent ConWeb. Two folders are present in this source: ConWeb V1.2 and ConWeb V2.0.

## ConWeb V1.2
The first version of the ConWeb NLU system was based on Rasa. To enhance its performance an NLU pipeline was designed to detect and overcome the errors of the Rasa model. Two NLU interpreters were devised:
  ### Heuristics interpreter
  It exploits some task-specific heuristics to infer the intent and the entities from the user utterance. Part of Speech and Dependency Grammars tags are employed to better understand which words of the utterance can be entities.
  ### OpenAI interpreter: 
  It exteracts intents and the entities using the GPT 3.5 language model

  ### Logs
  In this folder the logs record utterances, intents, entities and whether RASA or GPT 3.5 were used for the classification.


## ConWeb V2.0
ConWeb V2 collects the tests made with the latest version of ConWeb. This version uses OpenAI GPT4o 
  ### Logs 
  This folder collects logs that record user utterances, intent, and entities. The files are separated based on the website used during the interaction. 
