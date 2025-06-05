# Code the Dream AI Workspace
A workspace to develop hands-on, accessible AI teaching materials for [Code the Dream](https://codethedream.org/). This informal space is for experimenting with lesson plans, identifying core skills, and creating learning paths for Python 200 and AI modules. Student facing-material will be hosted at Code the Dream. 

## Plan
Our rough plan for the three weeks is as follows: 

- **Week 1: Hello, AI**: From large-language-models to chatbots.
- **Week 2: Retrieval-augmented generation (RAG)**: Building external knowledge-sources into LLM applications. 
- **Week 3: Agents**: Giving AI systems automomy to plan and use external tools.

For a more detailed discussion of the course plan, please [see the docs](https://ctdai.readthedocs.io/en/latest/). 

We are also building different [notebooks/](notebooks/README.md) to drop code for acquiring different skills and tools. Many of these are placeholders as we figure out the trajectory/learning path.

## Additional considerations
AI literacy is essential. Students should understand the basics of how LLMs work and what their limitations are, and the significant ethical dimensions of this work. We won’t have time to dive deeply into all these issues, but they should be acknowledged and incorporated into discussion, reflection, or light assignments. Some key points to cover: 

- LLMs are trained on vast internet data — this introduces *bias*, misinformation, and uneven quality.
- Ethical concerns include fairness, access, environmental impact, and explainability (there is a good overview of ethical considerations [here](https://libguides.amherst.edu/c.php?g=1350530&p=9969379)). 
- Many public discussions of AI are full of hype. Students should be equipped to think critically when people make outlandish claims (e.g., about AGI). This requires that they understand how the models work -- at least at a coarse level. 
  - Students should have a general grasp of concepts like transformers, attention mechanisms, and the strengths/limits of LLMs (e.g., text vs. visual reasoning).


## TO DO
- Consider adding brief assignments or discussion prompts to each notebook
- Build simple project templates for student teams: what assignments can be given each week?

## Installation
Built using uv. To install the dependences you can use `uv.lock` or `requirements.txt` (`pip install -r requirements.txt`). Please ask if help needed...

> I have pytorch installed w/cuda 12.6, so you might need to mess with that on your system (see https://pytorch.org/get-started/locally/).
