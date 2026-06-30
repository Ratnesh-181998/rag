# RAG


# 📚 Mastering Retrieval-Augmented Generation (RAG) - Handwritten Notes for AI/ML Interviews

- Understanding Retrieval-Augmented Generation (RAG) is becoming essential for anyone working with Generative AI, LLMs, and AI Agents.

- To strengthen my understanding, I created a comprehensive set of handwritten study notes covering the complete RAG pipeline in a simple, visual format.
  
## 📝 This page includes: 

- ✅ End-to-end RAG Pipeline
- ✅ Query Preprocessing
- ✅ Embedding Models
- ✅ Vector Databases
- ✅ Retrieval Methods
- ✅ Top-K Retrieval
- ✅ Context Augmentation
- ✅ Prompt Engineering
- ✅ Large Language Models (LLMs)
- ✅ Evaluation Metrics
- ✅ Chunking Techniques
- ✅ RAG Variants (Graph RAG, Agentic RAG, Self-RAG, CRAG, Hybrid RAG, Adaptive RAG & more)
- ✅ Advantages and Real-World Applications
- Creating handwritten notes helps simplify complex concepts and improves long-term retention, making them a valuable resource for interview preparation and practical implementation.

  <img width="770" height="1170" alt="image" src="https://github.com/user-attachments/assets/9aea0ed1-4df0-4168-9d41-1928b631743b" />

---
  
# When you ask an LLM a question, it does not write the full answer in one shot.


It goes step by step.

Let’s take a simple prompt:

“What is gravity?”

Step 1: The model receives your text.

At this point, it is just normal human language.

Step 2: The text is broken into smaller pieces.

These pieces are called tokens.

A token can be a word, part of a word, or a symbol.

For example:

What
is
grav
ity
?

Step 3: Each token is converted into a number.

The model cannot directly understand text.

So every token gets a token ID.

Now the sentence has become a list of numbers.

Step 4: Those numbers are converted into vectors.

A vector is just a long list of numbers that represents meaning.

This helps the model understand that some words are related to each other.

For example, “gravity” is closer to ideas like force, mass, earth, and physics.

Step 5: These vectors go through many processing blocks.

These blocks are called transformer layers.

You can think of each layer as one round of thinking.

In every round, the model asks:

Which words matter here?

Which tokens are related?

What context should I remember?

For example, if the prompt is long, the model needs to know which earlier words are important for the next word.

This is where attention is used.

Attention helps the model focus on the right parts of the input.

Step 6: After many such layers, the model creates a final internal understanding of the prompt.

It still has not written the answer.

It has only prepared the context.

Step 7: Now the model predicts the next token.

It looks at all possible tokens in its vocabulary and gives each one a probability.

For example, after “Gravity is a”, the model may think:

force → very likely
concept → possible
banana → unlikely

Step 8: A sampling method chooses the next token.

Sometimes it picks the most likely token.

Sometimes it picks from a group of likely tokens.

This is why the same prompt can sometimes produce slightly different answers.

Step 9: The selected token is added to the output.

Then the model repeats the same process again.

It predicts the next token.

Then the next.

Then the next.

That is why the answer appears word by word on the screen.

So the full flow looks like this:

Text
→ tokens
→ token IDs
→ vectors
→ processing layers
→ probabilities
→ next token
→ repeat
→ final answer

This is also why LLM performance is not only about the model.

It is also about inference.

How fast tokens are processed.

How memory is used.

How previous context is cached.

How decoding happens one token at a time.

Once you understand this pipeline, LLMs feel less mysterious.

<img width="792" height="1052" alt="image" src="https://github.com/user-attachments/assets/861166ca-d294-4bf7-a440-158b9a485aab" />

<img width="702" height="1294" alt="image" src="https://github.com/user-attachments/assets/0e8a2fd7-e522-47ca-a8a4-f19ff50ca31f" />
<img width="714" height="1288" alt="image" src="https://github.com/user-attachments/assets/92b1f2c4-37e9-44a8-b79d-4a58c88e11d0" />
<img width="650" height="660" alt="image" src="https://github.com/user-attachments/assets/078be29a-6a6b-43ac-a6f0-d0ebe9eaceb8" />


---

  
