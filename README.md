# unreasonble-word-vectors

Word vectors are competent at logical tasks: many word vector models easily beat human averages on the Reading section of the Scholastic Aptitude Test (SAT) (https://www.cs.princeton.edu/sites/default/files/uploads/eugene_tang.pdf). However, perhaps related to this rigidity, many models struggle with understanding metaphorical speech, and even exhibit racist and sexist tendencies (https://arxiv.org/abs/1607.06520).
 
The goal of this project is to research and prototype new word vector models, called Unreasonble Word Vectors, which can mitigate some of these undesirable features by being flexible, creative, and inclusive. I have one specific model in mind:
 
Many neural embeddings are trained on a value function paradigm that is perhaps too "reasonable": given a context, predict a word that fits that context, based on the corpus data. For example: "the cat ____ on the mat." The right answer, I suppose, is "sat", but that is not very interesting, precisely because the value function values predictable and uninteresting answers. So the idea is to use an "unreasonable", or metaphorical, value function: to the vanilla value function, add a regularizer function that insists that "crime" is equal to "disease" (https://web.stanford.edu/~jlmcc/papers/ThibodeauMcCBoroditsky09CogSciProc.pdf). Theoretically, this should have an effect, over the entire model, so that if "crime" and "disease" end up having similar embeddings in the model, perhaps "teacher" and "doctor" will, also: the goal is to make this unpredictable, but in an interesting way, that is, not random.