# ConWeb-Logs
This source is a collection of conversation logs obtained using ConWeb. ConWeb is a browser extension that, is able to parse the content of a webpage and enable navigation through voice commands.

This source comprises conversation logs collected during user studies for the voice agent ConWeb. Two folders are present in this source: ConWeb V1.2 and ConWeb V2.0.

## ConWeb V1.0
The first version of the ConWeb NLU system was based on Rasa and spaCy. To enhance its performance an NLU pipeline was designed to detect and overcome the errors of the Rasa/spaCy model: The system would use the RASA/spaCy model to perform intent and entity classification, if the confidence score was lower than a set treshold, the user utterance was sent first to a **heuristic interpreter** a rule based interpreter that used some problem specific heuristics to identify intents and entities. In case this step also failed, the last attempt at classification would be performed by the **OpenAI interpreter**. The OpenAI interpreter used the GPT 3.5 language model.

![immagine](https://github.com/user-attachments/assets/c2cac943-3060-4822-8018-3742b7bb4bd0)


### Logs
The logs in this folder were collected to assess the accuracy of the system and record the instances in which the RASA model failed and the OpenAI interpreter was invoked.
The logs record utterances, intents, entities and whether RASA or GPT 3.5 were used for the classification Below an example

![immagine](https://github.com/user-attachments/assets/44085634-41c5-4008-b057-6e599662ca73)


### legend
**id:** code for the utterance

**userId:** code for the session

**time:** time stamp with date (YYYY-MM-DD) and time (hh:mm:ss)

**sentence:** user utterance

**pred_intent:** intent classified by RASA

**pred_entities:** entities recognized by RASA

**true_intent:** final intent used

**true_entitie:** final entities used

**rasa_error:** true or false value expressed in 0 or 1 

**check_fp:** true or false value, expressed in 0 or 1, that says if GPT 3.5 was invoked or not to correct Rasa's predictions

**to_fix:** true or false value, expressed in 0 or 1, that tells whether the utterance is to be reclassified manually because the pipeline correction is wrong
  


## ConWeb V2.0
ConWeb V2 uses LLMs for all NLU and NLP tasks. OpenAI's GPT-4 model was used to perform intent and entity classification. The accuracy of the new NLU module was tested on a list of italian and english websites sampled randomly to represent a variety of domains.

  * [Wikipedia - Home Page](https://it.wikipedia.org)
  * [Poste Italiane - Home Page](https://www.poste.it)
  * [Today - Home Page](https://www.today.it)
  * [Open - Home Page](https://www.open.online)
  * [Android - Home Page](https://www.android.com)
  * [Beni Culturali - Home Page](https://www.beniculturali.it)
  * [Comune di Milano - Home Page](https://www.comune.milano.it)
  * [BBC - Home Page](https://www.bbc.co.uk)
  * [Wall Street Journal - Home Page](https://www.wsj.com)
  * [W3 - Home Page](https://www.w3.org)

 ## Logs
 The logs in this folder record user utterances, intent, and entities. The files are separated based on the tested website. Furthermore, in each file. utterances are clustered by intent. Below an example

```
Intent: Navigare

Expected result: {'intent': 'navigare', 'entities': ['Culture'] (at least one)}

Utterance: apri Culture

Result: {'intent': 'navigare', 'entities': ['Culture']}

```

## Dataset Authors
Roberto Ricci, Fabio Tresoldi, Ludovica Piro, Emanuele Pucci
