# Low_Resource_KBP
knowledge graph population in low resource conditions


The file "*Few-Shot_ED.json.zip*" is the ***FewEvent*** dataset for the paper accepted by WSDM 2020 ***["Meta-Learning with Dynamic-Memory-Based Prototypical Network for Few-Shot Event Detection"](https://arxiv.org/abs/1910.11621)***


## Source of Raw Data
* We first scale up the number of event types in existing datasets, including the [ACE-2005 corpus](http://projects.ldc.upenn.edu/ace/), and [TAC-KBP-2017 Event Track Data](https://tac.nist.gov/2017/KBP/Event/index.html).

* We then import and extend some new event types based on an [automatically-labeled event data](https://github.com/acl2017submission/event-data), from Freebase and Wikipedia, constrained to specific domains such as music, film, sports, education, etc.

## Data Structure
In "*Few-Shot_ED.json.zip*"，the key is "*event type label*", the value is the event instances.

{event_type_label1: \[instance1, instance2, ...\], event_type_label2: ...}

### example of an event instance: 
(Note that the sentence should be cleaned, e.g., To expand abbreviations)

\["In trucks and on foot they came to the town of Safwan", "came", \[7, 6, 12\]\] 

* "In trucks and on foot they came to the town of Safwan" is an event mention
* "came" is trigger
* 7 means the distance from trigger "came" to the beginning of the sentence
* 6 means the distance from trigger "came" to the ending of the sentence
* 12 means the sentence length

