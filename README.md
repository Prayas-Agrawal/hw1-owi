# Complex Vs transformers
Members: Prayas Agrawal
## FB15k (ValmaskMode: sr?)
### Complex:
(MRR: 0.1634 , hits@1: 0.1601, hits@10: 0.3503 )
### Transformers (trainMode: score):  
(MRR: 0.1189 , hits@1: 0.1488, hits@10: 0.3225 ) 
### Transformers (trainMode: mlm):    
(MRR: 0.1352 , hits@1: 0.1456, hits@10: 0.3291 )

## FB15k (ValmaskMode: ?ro)
### Transformers (trainMode: score):  
(MRR: 0.0913 , hits@1: 0.1376, hits@10: 0.3165 )
### Transformers (trainMode: mlm):    
(MRR: 0.0996 , hits@1: 0.1105, hits@10: 0.2331 )

## WN18RR (ValmaskMode: sr?)
### Complex:  
(MRR: 0.2822 , hits@1: 0.2161, hits@10: 0.3541 )
### Transformers (trainMode: score):  
(MRR: 0.2273 , hits@1: 0.2271, hits@10: 0.3267 )
### Transformers (trainMode: mlm):    
(MRR: 0.2410 , hits@1: 0.1902, hits@10: 0.3594 )

## WN18RR (ValmaskMode: ?ro)
### Transformers (trainMode: score):  
(MRR: 0.2002 , hits@1: 0.2147, hits@10: 0.3044 )
### Transformers (trainMode: mlm):    
(MRR: 0.2114 , hits@1: 0.1891, hits@10: 0.3208 )

## Methodology
Encoder only model inspired from BERT
For every query in dataset, negative samples were introduced by replacing the s/o in the query with random entities from data. If the negatives were also present in test dataset, then they were assigned a gold label of 1. Docuements were retrieved, but for finding recall, top-k sentences of top-p documents were retrieved.