---
title: Construction contract risk identification based on knowledge-augmented language models
authors: Saika Wong, Chunmo Zheng, Xing Su, Yinqiu Tang
year: 2024
DOI: 10.1016/j.compind.2024.104082
Create_time:
---

1. There are two knowledge bases: project clauses base and expert knowledge base.
	2. Project clauses base:
	    - Stores potentially risky contract clauses that need to be reviewed
	    - Contains fields: ID, Embeddings, Clause_type, Project_clauses
	    - Clause_type stores the section name
	    - Project_clauses stores the detailed clause content
	    - Embeddings stores the vector representation of Project_clauses
	3. Expert knowledge base:
	    - Stores pairs of case clauses (identified as risky in past) and their reviews
	    - Contains fields: ID, Embeddings, Checkpoints, Case_clauses, Reviews
	    - Checkpoints stores risk identification requirements from expert checklists
	    - Case_clauses stores risky clauses from past contracts
		    - Reviews stores expert reviews explaining risks in Case_clauses
	
2. Relationship:
    - One checkpoint can be linked to multiple case clauses
    - Each review is for a specific (checkpoint, case clause) pair
3. Checkpoints cover risk categories like contractual basics, payments, schedule, liabilities etc.
    - Can be abstract (logical reasoning) or concrete (extracting specifics)
3. Reviews have 3 parts: conclusion, relevant clause content, rationale
4. Before storage, contract text is vectorized by:
    - Parsing into chunks based on clause sections to preserve semantics
    - Embedding each chunk into a vector using a text vectorizer
    - Storing the chunk text and vector in the knowledge base