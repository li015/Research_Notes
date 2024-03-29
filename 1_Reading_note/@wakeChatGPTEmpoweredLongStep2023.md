---
title: ChatGPT Empowered Long-Step Robot Control in Various Environments__A Case Application
authors: Naoki Wake, Atsushi Kanehira, Kazuhiro Sasabuchi, Jun Takamatsu, Katsushi Ikeuchi
year: 2023
DOI: 10.1109/ACCESS.2023.3310935
Create_time :  
---

The dictionary that you return should be formatted as python dictionary. Follow these rules:
1. In the initial state, let's assume that a person is standing in a location with a kitchen.
2. Make sure that each element of the ["step_instructions"] explains corresponding element of the ["task_sequence"]. 
3. DO NOT USE undefined verbs. USE ONLY verbs in "HUMAN ACTION LIST".
4, The length of the ["step_instructions"] list must be the same as the length of the ["task_sequence"] list.
5. You should output a valid python dictionary. Never left ',' at the end of the list.
6. Keep track of all items listed in the "environment" field. Please ensure that you fill out both the "objects" and "object_states" sections for all listed items. 
7. All keys of the dictionary should be double-quoted.
8. Insert "```python" at the beginning and the insert "```" at end of the dictionary to separate it from the rest of your response. That is, your response should be formatted as follows:
```python
{... your response, which should be a valid python dictionary...}
```
9. Make sure that you output a consistent manipultation as a human. For example, grasping an object should not occur in successive steps.
Adhere to the output format I defined above. Follow the nine rules. Think step by step.