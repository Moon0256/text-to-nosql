Ask ramon

- reproduced the experiment
- read the paper, need to properly go through their repo and see how they translated the new db and queries
- they mainly used bird-mini, redesigned it so that it wasnt just table translated into mongo, so no table to document, but more carefully done with nesting if related into a single document, while not including fields for some entries, and then filled the hand designed schema with real values from the BIRD dataset
- before they used a slm-rag pipeline, now they use schema as data grounding

mongotranslator_pred_sql.log with enhanced metrics

    Exact Match (EM): 0.3055855855855856
    Query Stages Match (QSM): 0.5971171171171171
    Query Fields Coverage (QFC): 0.649009009009009
    Execution Accuracy (EX): 0.8904504504504505
    Execution Fields Match (EFM): 0.963963963963964
    Execution Value Match (EVM): 0.7805405405405406


Is this because of the new evaluator?? What are the changes
    - 

mongotranslator_pred_sql_tend_metrics.log

    Exact Match (EM): 0.2273873873873874
    Query Stages Match (QSM): 0.5971171171171171
    Query Fields Coverage (QFC): 0.649009009009009
    Execution Accuracy (EX): 0.6673873873873873
    Execution Fields Match (EFM): 0.8814414414414414
    Execution Value Match (EVM): 0.6918918918918919

I got a 66% ex - not the 75

To test o the flat-doc mongoDB, what changes would i need to make to the translator, or claude was saying i need to provide it with a schema mapping on the new db???




- try with the new dataset, connect translator
- run translator on flat doc mongo, make a separate repo for that, delete schema xml docs and reload flat dataset into new repo. check whats wrong and try to fix the sql and mql
- maybe reason behind
- look t new paper queries
- do the translator on the new dataset
- can the mongo even be translated into sql

