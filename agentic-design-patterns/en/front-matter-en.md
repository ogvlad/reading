# Agentic Design Patterns — Front Matter
**A Hands-On Guide to Building Intelligent Systems**
*Antonio Gulli*

---

## Dedication

To my son, Bruno, who at two years old, brought a new and brilliant light into my life. As I explore the systems that will define our tomorrow, it is the world you will inherit that is foremost in my thoughts.

To my sons, Leonardo and Lorenzo, and my daughter Aurora — My heart is filled with pride for the women and men you have become and the wonderful world you are building.

This book is about how to build intelligent tools, but it is dedicated to the profound hope that your generation will guide them with wisdom and compassion. The future is incredibly bright, for you and for us all, if we learn to use these powerful technologies to serve humanity and help it progress.

With all my love.

---

## Acknowledgments

I would like to express my sincere gratitude to the many individuals and teams who made this book possible.

First and foremost, I thank Google for adhering to its mission, empowering Googlers, and respecting the opportunity to innovate. I am grateful to the Office of the CTO for giving me the opportunity to explore new areas, for adhering to its mission of "practical magic," and for its capacity to adapt to new emerging opportunities.

I would like to extend my heartfelt thanks to Will Grannis, our VP, for the trust he puts in people and for being a servant leader. To John Abel, my manager, for encouraging me to pursue my activities and for always providing great guidance with his British acumen.

I extend my gratitude to Antoine Larmanjat for our work on LLMs in code, Hann Hann Wang for agent discussions, and Yingchao Huang for time series insights. Thanks to Ashwin Ram for leadership, Massy Mascaro for inspiring work, Jennifer Bennett for technical expertise, Brett Slatkin for engineering, and Eric Schen for stimulating discussions. The OCTO team, especially Scott Penberthy, deserves recognition. Finally, deep appreciation to Patricia Florissi for her inspiring vision of Agents' societal impact.

My appreciation also goes to Marco Argenti for the challenging and motivating vision of agents augmenting the human workforce. My thanks also go to Jim Lanzone and Jordi Ribas for pushing the bar on the relationship between the world of Search and the world of Agents.

I am also indebted to the Cloud AI teams, especially their leader Saurabh Tiwary, for driving the AI organization towards principled progress. Thank you to Salem Haykal, the Area Technical Leader, for being an inspiring colleague. My thanks to Vladimir Vuskovic, co-founder of Google Agentspace, Kate (Katarzyna) Olszewska for our Agentic collaboration on Kaggle Game Arena, and Nate Keating for driving Kaggle with passion.

A special thanks to Yingchao Huang for being a brilliant AI engineer with a great career in front of you, Hann Wang for challenging me to return to my interest in Agents after an initial interest in 1994, and to Lee Boonstra for your amazing work on prompt engineering.

I extend my gratitude to Demis Hassabis, Pushmeet Kohli, and the entire GDM team for their passionate efforts in developing Gemini, AlphaFold, AlphaGo, and AlphaGenome, and for their contributions to advancing science for the benefit of society.

A special thanks to Patti Maes, who pioneered the concept of Software Agents in the 90s — your vision back in '91 became a reality today.

I also want to extend my gratitude to Paul Drougas and all the Publisher team at Springer for making this book possible.

My heartfelt thanks go to Marco Fago for his immense contributions, Mahtab Syed for his coding work, and Ankita Guha for her incredibly detailed feedback. The book was significantly improved by Priya Saxena, Jae Lee, and Mario da Roza.

All my royalties are donated to Save the Children.

---

## Foreword
*Saurabh Tiwary, VP & General Manager, CloudAI @ Google*

The field of artificial intelligence is at a fascinating inflection point. We are moving beyond building models that can simply process information to creating intelligent systems that can reason, plan, and act to achieve complex goals with ambiguous tasks. These "agentic" systems represent the next frontier in AI.

"Agentic Design Patterns" arrives at the perfect moment. The book rightly points out that the power of large language models — the cognitive engines of these agents — must be harnessed with structure and thoughtful design. Just as design patterns revolutionized software engineering by providing a common language and reusable solutions, the agentic patterns in this book will be foundational for building robust, scalable, and reliable intelligent systems.

The metaphor of a "canvas" for building agentic systems resonates deeply with our work on Google's Vertex AI platform. By exploring patterns from prompt chaining and tool use to agent-to-agent collaboration, self-correction, safety and guardrails, this book offers a comprehensive toolkit for any developer looking to build sophisticated AI agents.

---

## A Thought Leader's Perspective: Power and Responsibility
*Marco Argenti, CIO, Goldman Sachs*

Of all the technology cycles I've witnessed over the past four decades — from the birth of the personal computer and the web, to the revolutions in mobile and cloud — none has felt quite like this one.

If the last eighteen months were about the engine — the breathtaking, almost vertical ascent of Large Language Models — the next era will be about the car we build around it. It will be about the frameworks that harness this raw power, transforming it from a generator of plausible text into a true agent of action.

The first time I experimented with one of the new agentic coding tools, I felt that familiar spark of magic. I tasked it with migrating a charity website to a modern CI/CD environment. For twenty minutes, it went to work, asking clarifying questions, requesting credentials, and providing status updates. It felt less like using a tool and more like collaborating with a junior developer. When it presented me with a fully deployable package, complete with impeccable documentation and unit tests, I was floored.

Of course, it wasn't perfect. It made mistakes. It got stuck. It required my supervision and, crucially, my judgment to steer it back on course. Peeking into its "chain of thought" was like watching a mind at work — messy, non-linear, full of starts, stops, and self-corrections, not unlike our own human reasoning.

This is the promise of agentic frameworks. It's the difference between a static subway map and a dynamic GPS that reroutes you in real-time.

As exhilarating as this new frontier is, it brings a profound sense of responsibility. The stakes are immeasurably high. An agent that makes a mistake while creating a recipe is a fun anecdote. An agent that makes a mistake while executing a trade, managing risk, or handling client data is a real problem.

The hard truth is that you cannot simply overlay these powerful new tools onto messy, inconsistent systems and expect good results. Messy systems plus agents are a recipe for disaster. We must invest in clean data, consistent metadata, and well-defined APIs.

Ultimately, this journey is not about replacing human ingenuity, but about augmenting it. The world is asking every engineer to step up. I am confident we are ready for the challenge.

---

## Introduction (Preface)

Welcome to "Agentic Design Patterns: A Hands-On Guide to Building Intelligent Systems."

We see a clear evolution from simple, reactive programs to sophisticated, autonomous entities capable of understanding context, making decisions, and interacting dynamically with their environment and other systems. These are the intelligent agents and the agentic systems they comprise.

Think of building intelligent systems as creating a complex work of art or engineering on a canvas. This canvas is the underlying infrastructure and frameworks that provide the environment and tools for your agents to exist and operate.

**What are Agentic Systems?**

At its core, an agentic system is a computational entity designed to perceive its environment, make informed decisions based on those perceptions, and execute actions to achieve goals autonomously. Unlike traditional software, agents exhibit a degree of flexibility and initiative.

Agentic systems are characterized by:
- **Autonomy** — acting without constant human oversight
- **Proactiveness** — initiating actions towards their goals
- **Reactiveness** — responding effectively to changes in their environment
- **Goal-orientation** — constantly working towards objectives
- **Tool use** — interacting with external APIs, databases, or services
- **Memory** — retaining information across interactions

**Why Patterns Matter**

Agentic design patterns are not rigid rules, but battle-tested templates that offer proven approaches to standard design and implementation challenges. This book extracts 21 key design patterns that represent fundamental building blocks for constructing sophisticated agents.

**Frameworks Used in This Book**

- **LangChain / LangGraph** — flexible chaining of language models and components
- **Crew AI** — orchestrating multiple AI agents, roles, and tasks
- **Google Agent Developer Kit (ADK)** — building, evaluating, and deploying agents

---

## What Makes an AI System an Agent?

An AI agent is a system designed to perceive its environment and take actions to achieve a specific goal. It's an evolution from a standard LLM, enhanced with the abilities to plan, use tools, and interact with its surroundings.

An Agentic AI follows a five-step loop:

1. **Get the Mission** — You give it a goal
2. **Scan the Scene** — It gathers all necessary information
3. **Think It Through** — It devises a plan of action
4. **Take Action** — It executes the plan
5. **Learn and Get Better** — It observes outcomes and adapts

**The Spectrum of Agent Complexity**

- **Level 0: The Core Reasoning Engine** — LLM without tools, memory, or environment interaction. Responds solely based on pretrained knowledge.

- **Level 1: The Connected Problem-Solver** — LLM connected to external tools (search, RAG, APIs). Can act across multiple steps in the outside world.

- **Level 2: The Strategic Problem-Solver** — Multi-tool use with context engineering — the strategic process of selecting, packaging, and managing the most relevant information for each step. Proactive, self-improving.

- **Level 3: Collaborative Multi-Agent Systems** — Multiple specialized agents working in concert, mirroring a human organization with division of labor and coordinated effort.

**The Future of Agents: Top 5 Hypotheses**

1. **Generalist Agents** — evolving from narrow specialists into true generalists capable of managing complex, long-term goals
2. **Deep Personalization and Proactive Goal Discovery** — agents that anticipate needs and discover goals before you articulate them
3. **Embodiment and Physical World Interaction** — agents integrated with robotics, operating in the physical world
4. **The Agent-Driven Economy** — highly autonomous agents as active participants in economic activity
5. **Goal-Driven, Metamorphic Multi-Agent Systems** — systems that declare a goal and autonomously self-organize, self-modify, and self-improve

**Market context:** By end of 2024, AI agent startups had raised more than $2 billion; market valued at $5.2 billion. Expected to reach nearly $200 billion by 2034.
