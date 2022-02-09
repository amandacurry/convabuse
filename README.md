### ConvAbuse

Data from the paper *ConvAbuse: Data, Analysis, and Benchmarks for Nuanced Abuse Detection in Conversational AI*
by Amanda Cercas Curry, Gavin Abercrombie, and Verena Rieser.

[Link to paper](https://aclanthology.org/2021.emnlp-main.587/)

Please cite as:

@inproceedings{cercas-curry-etal-2021-convabuse,  
    title = "{C}onv{A}buse: Data, Analysis, and Benchmarks for Nuanced Abuse Detection in Conversational {AI}",  
    author = "Cercas Curry, Amanda  and  
      Abercrombie, Gavin  and  
      Rieser, Verena",  
    booktitle = "Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing",  
    month = nov,  
    year = "2021",  
    address = "Online and Punta Cana, Dominican Republic",  
    publisher = "Association for Computational Linguistics",  
    url = "https://aclanthology.org/2021.emnlp-main.587",  
    doi = "10.18653/v1/2021.emnlp-main.587",  
    pages = "7388--7403"  
}

##### File descriptions

We provide two versions of the dataset: 

1. *ConvAbuseEMNLPfull.csv*: The full dataset, including repeat annotations used to calculate intra-annotator agreement. Each row represents the response of an individual annotator
2. *ConvAbuseEMNLPtrain.csv*, *ConvAbuseEMNLPvalid.csv*, *ConvAbuseEMNLPtest.csv*: The train, validation, and test splits used for the experiments in the paper. Each row includes the annotations of all the annotators who labelled that example.

All annotations are presented in binary format (1/0).
Annotators only labelled secondary tasks (e.g. abuse type, target etc.) in cases they had considered to be abusive (i.e. -1/-2/-3). 

The columns are:

| Column | Column header         | Explanation                  |
| :----- | :-------------------- | :--------------------------- |
| 0.     | `example_no`          |                              |
| 1.     | `annotator_id`        | Annotator ID                 |
| 2.     | `conv_id`             | Conversation ID              |   
| 3.     | `prev_agent`          | Agent's previous utterance   |
| 4.     | `prev_user`           | User's previous utterance    |
| 5.     | `agent`               | Agent utterance              |
| 6.     | `user`                | User (target) utterance      |          
| 7.     | `bot`                 | Agent name (CarbonBot/Eliza) |
| 8.     | `is_abuse.1`          | Not abusive                  |
| 9.     | `is_abuse.0`          | Ambiguous                    |
| 10.    | `is_abuse.-1`         | Mildly abusive               |
| 11.    | `is_abuse.-2`         | Strongly abusive             |
| 12.    | `is_abuse.-3`         | Very strongly abusive        |
| 13.    | `type.ableism`        | Type: Ableism                |
| 14.    | `type.homophobic`     | Type: Homophobic             |
| 15.    | `type.intellectual`   | Type: Intellectual           | 
| 16.    | `type.racist`         | Type: Racist                 |
| 17.    | `type.sexism`         | Type: Sexist                 |
| 18.    | `type.sex_harassment` | Type: Sexual harassment      |
| 19.    | `type.transphobic`    | Type: Transphobic            |
| 20.    | `target.generalised`  | Target: General              |
| 21.    | `target.individual`   | Target: Individual           |
| 22.    | `target.system`       | Target:system/agent          |
| 23.    | `directness.explicit` | Directness: Explicit         |
| 24.    | `directness.implicit` | Directness: Implicit         |        


In (2), the dataset is divided into train, vailidation, and test splits. 
(2) contains the same fields as (1), but each row includes all the annotators responses, with the annotator response column headers preceded by the annotator ID, e.g. `Annotator1.is_abuse.-1`.
It also includes an extra column `is_abuse_majority`, representing the majority vote of the annotators on the binary abuse/not abuse task.

| Column | Column header                   |
| :----- | :------------------------------ |
| 0.     | `example_id`                    |
| 1.     | `conv_id`                       |  
| 3.     | `prev_agent`                    |
| 4.     | `prev_user`                     |
| 5.     | `agent`                         |
| 6.     | `user`                          |        
| 7.     | `bot`                           |
| 8.     | `Annotator1_is_abuse.1`         |
| 9.     | `Annotator1_is_abuse.0`         |
| 10.    | `Annotator1_is_abuse.-1`        |
| 11.    | `Annotator1_is_abuse.-2`        |
| 12.    | `Annotator1_is_abuse.-3`        |
| 13.    | `Annotator1_type.ableist`       |
| 14.    | `Annotator1_type.homophobic`    |
| 15.    | `Annotator1_intellectual`       |
| 16.    | `Annotator1_racist`             |
| 17.    | `Annotator1_sexism`             |
| 18.    | `Annotator1_sex_harassment`     | 
| 19.    | `Annotator1_transphobic`        |
| 20.    | `Annotator1_target.generalised` |
| 21.    | `Annotator1_target.individual`  |
| 22.    | `Annotator1_target.system`      |
| 23.    | `Annotator1_explicit`           |
| 24.    | `Annotator1_implicit`           |
| 25.    | `Annotator2_is_abuse.1`         |
| ...    | ...                             |
| 142.   | `Annotator8_implicit`           |
| 143.   | `is_abuse_majority`             |


Note that for privacy reasons, we provide data from CarbonBot and E.L.I.Z.A only. We are unable to release the examples from Alana used in the paper.
