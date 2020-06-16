The code tries to answer task questions.
Our task questions are: "What do we know about virus genetics, origin, and evolution?", "What do we know about the virus origin and management measures at the human-animal interface?"
We take abstarcts in the metadata.csv as original data and assume that they contain all the answers.
We use Bert as our model. Bert Model with a span classification head on top for extractive question-answering tasks like SQuAD (a linear layers on top of the hidden-states output to compute span start logits and span end logits)
The answer_question function take question, title and abstract as input, and return the answers. We ignored the answer "[SEP]", "[CLS]" and answers which are less than 3 words.
For each abstract, we do answer_question to answer the question.
We run the answer_question on both first 100 abstracts and random sampled 1000 abstracts. The results are within the notebook.
