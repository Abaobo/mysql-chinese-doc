## 8.9 Controlling the Query Optimizer

MySQL provides optimizer control through system variables that affect how query plans are evaluated, switchable optimizations, optimizer and index hints, and the optimizer cost model. 

The server also maintains statistics about column values, although the optimizer does not yet use this information. 