# Heuristics for automatically identifying adpositional expressions

Automatically (heuristically) identified single-word and multi-word prepositional expressions.
Each token has an additional column (the 20th column for the .conllulex format) containing its predicted category.
The value can be one of the following:
* -: is not and does not belong to a prepositional expression
* *: is a single-word prepositional expression
* N:1**: is the first word in a multi-word prepositional expression (where N >= 1 is the index of the multiword expression in the current sentence)
* N:M: is the Mth word in a multi-word prepositional expression (where M > 1 and N >= 1 is the index of the multiword expression in the current sentence)

Note that only tokens with labels ending in an asterisk (*) should get a supersense.

## Files

streusle.ud_dev.auto_id.conllulex
streusle.ud_test.auto_id.conllulex
streusle.ud_train.auto_id.conllulex


## Performance

### strict evaluation as used in Schneider et al., 2018

|       | P     | R     | F     |
|:----  |:-----:|:-----:|:-----:|
| test  | 0.888 | 0.896 | 0.892 |

### relaxed evaluation

|       | P     | R     | F     |
|:----  |:-----:|:-----:|:-----:|
| test  | 0.906 | 0.914 | 0.910 |
| train | 0.965 | 0.925 | 0.945 |
| dev   | 0.903 | 0.917 | 0.910 |