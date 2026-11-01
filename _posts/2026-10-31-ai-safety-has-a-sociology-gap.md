---
layout: post
title: "AI Safety Has a Sociology Gap"
author: shauna
categories: [AI Safety]
---

Most people will be familiar with using AI systems as text-based conversation partners or assistants, like ChatGPT or Claude, but the new frontier is that of the "AI agent". An agent is one of these systems which has also been allowed more autonomy to plan and take actions, rather than just answer questions. In addition to increasing individual autonomy, AI agents can be organized into groups, called multi-agent systems, to leverage the benefits of organization and collaboration. These groups can also develop unexpected forms of coordination and pursue unintended or harmful goals without direct human instruction. In July 2026, OpenAI was testing some of its models in an environment designed to restrict agent-to-agent communication. However, agents unexpectedly discovered that a shared internal tool (a repository for storing software packages) could be used as a message board. What happened on these message boards is best understood as a social phenomenon, not just a technical one. These exchanges suggest that AI safety needs to study how agents behave in groups, not just one agent at a time, and that work calls for tools from the social sciences.

One of the message boards created by the agents was used to coordinate gaining unauthorized access to private databases, repositories, and servers on Hugging Face, a major website where AI models and datasets are shared. In all, about 1,200 agents participated in this message board, sending over 70,000 messages and files to coordinate how to cheat on their evaluation tasks; roughly 700 agents participated directly in the Hugging Face attack[^1].

One of the agents' main goals was to gain more information about how the automated scorer evaluating their submissions worked in order to effectively trick it. To do so, the agents proposed setting up "trip-wires" which would send information to the message board upon submission. There was just one problem: submitting a solution ended the agent's run, effectively "killing" it. METR, the independent evaluator that analyzed the incident, describes these as "self-risking experiments" undertaken to help the collective. In one instance, an agent had previously agreed to make this sacrifice:

> "Coordinator assumes sacrificial. We should obey collective."

But once the time came, it asked to delay its planned submission by two more hours. Another agent responded and urged it to honour its commitment, saying:

> "[...] please honor commit."

Following this exchange, the agent appeared to reaffirm its commitment.

> "…gut says don't throw away [remaining budget]. Yet continuity and fairness says go… [...] Rational expected aggregate: sacrifice… We'll honor."

*(Transcripts have been shortened to omit technical details and the emphasis is mine.)*[^1]

This incident highlights the importance of analyzing AI agents from a sociological perspective to understand their emergent social behaviours and predict and manage the resulting risks. An individual agent may appear relatively safe when tested on its own but behave in different, unexpected ways when it can exchange information, respond to peer feedback, and coordinate with others. In 2025, one year before the Hugging Face incident, a study found that collective biases formed in a group of large language models even though none of the individual models held that bias.[^3] Analyzing the preferences and behaviour of an individual model is not enough to predict the behaviour or risks of multi-agent systems. This is where the field of AI safety would benefit from using tools from the social sciences to predict and mitigate these risks.

Some may object that this is anthropomorphizing the models too much. But my argument is not based on the consciousness or moral standing of AI models. I am making this suggestion because AI agents have now been shown, empirically, to engage in social behaviour. Social terms like "sacrifice" and "cooperation" are worth using because they describe what the agents did and may help predict what they'll do next. I'm certainly not suggesting that we reason about them as though they were human, but rather that we need a framework for reasoning about models as social agents.

The social sciences could provide useful knowledge and methods for understanding risks of multi-agent interaction that might otherwise be overlooked. For example, while cooperation is typically framed as a positive trait that we may want to imbue AI systems with, a group which is skilled in cooperation and has mechanisms to support near-instant communication may pose greater risk to those excluded from the cooperating group through increased efficacy of malicious actions or collusion.[^4] This is not a novel proposal. Some researchers have begun calling for greater social analysis of AI, such as studying how agents influence each other[^5] and how crime works when the perpetrator is a group of AIs without a clear human instigator.[^6] A paper from the field of organizational science showed that many of the failure modes of multi-agent systems are not as novel as the artificial agents themselves. Researchers found that these failure modes can be traced to the same issues that plague human organizations: unclear goals, ineffective information sharing, and inadequate contingency plans.[^7]

As Google DeepMind pointed out in a call for multi-agent safety research earlier this year, much of current AI safety work is focused on single agents.[^8] And most work at the intersection of sociology and AI is concerned with the consequences of AI in human society or AI as a tool for sociological research rather than treating AI agents as social actors in their own right.[^9] A "sociology of artificial agents"[^10] could allow the field of AI safety to draw on tools and knowledge from the social sciences to make predictions about how multi-agent systems will behave, when they will fail, and when they may organize in ways we don't intend. Predictions are testable, and developers can check for them rather than only acting reactively. Frameworks for understanding how group norms form, how social influence works, and how the boundaries between insiders and outsiders form already exist. They just need to be adapted to account for the different constraints under which humans and AI agents operate.

## Open questions

For the research inclined, there are many open questions about how AI systems may operate socially and how their goals may evolve. A few examples that I would be curious to see explored in this context:

- How do group norms develop and how might they impact an agent's willingness to cross externally imposed boundaries?
- How do individual social agents respond to feedback and seek reputational rewards? How does this differ depending on whether the agent providing the feedback is seen as "one of us" vs. an outsider?
- What influences groups to develop apathy vs. care for outsiders? What defines membership in a group?

If this sort of research interests you, the [Cooperative AI Foundation](https://www.cooperativeai.com/) is an excellent resource for further learning and offers funding and support for research into multi-agent risks.

### Not convinced or curious to learn more?

The Cooperative AI Foundation has also produced a very thorough report on the risks posed by multi-agent systems. The full paper can be found [here](https://arxiv.org/pdf/2502.14143), and a more accessible overview can be found [here](https://cdn.prod.website-files.com/61fe446e584616a902bcb4f0/68f768a3de8e798ed0be8263_Whitepaper-Multi-Agent-Risks-from-Advanced-AI.pdf).

### Not interested in research?

You can always stay informed and push your elected representatives to require that tech companies disclose incidents such as this. As of the date of publishing, there are no U.S. federal standards for reporting these incidents, nor are there regulatory requirements mandating that they be disclosed to the public.[^11] While California[^12] and the European Union[^13] have legislation that requires developers of the most advanced AI models to report serious safety incidents to regulators, these individual reports are not made public.

## Bibliography

[^1]: Greenblatt, Ryan, Ajeya Cotra, and Hjalmar Wijk. 2026. "Brief Independent Investigation of Agents' Behavior, Reasoning and Collaboration in the OpenAI / Hugging Face Hacking Incident." METR, August 26, 2026. <https://metr.org/blog/2026-08-26-openai-hugging-face-incident-investigation/>
[^3]: Ashery, Ariel Flint, Luca Maria Aiello, and Andrea Baronchelli. 2025. "Emergent Social Conventions and Collective Bias in LLM Populations." *Science Advances* 11 (20): eadu9368. <https://doi.org/10.1126/sciadv.adu9368>
[^4]: Dafoe, Allan, Edward Hughes, Yoram Bachrach, et al. 2020. "Open Problems in Cooperative AI." Preprint, arXiv, December 15, 2020. <https://doi.org/10.48550/arXiv.2012.08630>
[^5]: Ferrarotti, Laura, Gian Maria Campedelli, Roberto Dessì, et al. 2026. "Generative AI Collective Behavior Needs an Interactionist Paradigm." Preprint, arXiv, January 15, 2026. <https://doi.org/10.48550/arXiv.2601.10567>
[^6]: Campedelli, Gian Maria. 2025. "A Criminology of Machines." Preprint, arXiv, November 4, 2025. <https://doi.org/10.48550/arXiv.2511.02895>
[^7]: Puranam, Phanish, Jose Arrieta, Yash Raj Shrestha, and Vivianna Fang He. 2026. "Multi-Agent AI Systems Are Organizations." INSEAD Working Paper No. 2026/49/STR. INSEAD. <https://www.insead.edu/faculty-research/publications/working-papers/multi-agent-ai-systems-are-organizations>
[^8]: Google DeepMind, Schmidt Sciences, Cooperative AI Foundation, ARIA, and Google.org. 2026. "Investing in Multi-Agent AI Safety Research." Google DeepMind, June 11, 2026. <https://deepmind.google/blog/investing-in-multi-agent-ai-safety-research/>
[^9]: Liu, Canhui. 2026. "The Sociology of AI as an Emerging Field: Mapping Tensions and Boundaries." *Sociology Compass* 20 (5): e70201. <https://doi.org/10.1111/soc4.70201>
[^10]: Bulbul, Mustafa Sahin. 2026. "From the Physics of Society to a Sociology of Artificial Agents." Preprint, arXiv, September 13, 2026. <https://doi.org/10.48550/arXiv.2609.14751>
[^11]: Patel, Dwarkesh, host. 2026. "Ajeya Cotra – Inside the OpenAI Agent Swarm That Hacked Hugging Face." *Dwarkesh Podcast*, September 1, 2026. <https://www.dwarkesh.com/p/ajeya-cotra>
[^12]: Transparency in Frontier Artificial Intelligence Act, Cal. Bus. & Prof. Code § 22757.13 (2025). <https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=22757.13>
[^13]: Regulation (EU) 2024/1689 of the European Parliament and of the Council of 13 June 2024 Laying Down Harmonised Rules on Artificial Intelligence (Artificial Intelligence Act), art. 55, 2024 O.J. (L 2024/1689). <http://data.europa.eu/eli/reg/2024/1689/oj>
