# Travel Itinerary LLM Agent Framework Evaluation

## Overview

This exercise aimed to explore, implement, and evaluate LLM-based agentic frameworks to enhance productivity in the travel domain. Specifically, the team designed a **travel itinerary chatbot** capable of collecting user preferences, recommending destinations and activities, and generating detailed itineraries for a group of graduate students. The project involved hands-on prototyping, functionality testing, and comparative assessment of two state-of-the-art agentic frameworks: **AutoGen** and **CrewAI**.

## Tools & Frameworks Used

- **Python 3.x**
- **Jupyter/IPython Notebooks**
- **AutoGen (Microsoft)**
- **CrewAI**
- **OpenAI GPT-3.5-turbo API**
- **Supporting libraries:** pandas, langchain, crewai_tools, etc.

## Business Objective

**Key Questions:**
- How can LLM-based agentic frameworks automate and enhance the process of customized travel planning?
- What are the comparative strengths and weaknesses of competing agentic approaches (single-agent vs. multi-agent) in real-world business scenarios?
- Which framework best supports the desired mix of scalability, user experience, customization, and ethical compliance?

**Project Task:**  
Build, evaluate, and compare travel planning agents using at least two LLM-based frameworks. Assess each for ease of development, quality of output, flexibility, scalability, costs, and ethical considerations. Prepare findings for class discussion.

## Exercise Structure & Methods

### 1. Project Foundations & Required Readings

This project is informed by foundational concepts and best practices in LLM agent design as presented by Andrew Ng and the DeepLearning.AI team. These readings are essential for understanding the agentic approaches implemented in our travel itinerary planning exercise:

- **How Agents Can Improve LLM Performance:** Explains why agent workflows (including iteration, planning, and collaboration) dramatically boost LLM utility compared to simple prompting.  
[https://www.deeplearning.ai/the-batch/how-agents-can-improve-llm-performance/](https://www.deeplearning.ai/the-batch/how-agents-can-improve-llm-performance/)

- **Agentic Design Patterns Series:**  
  - Reflection: LLMs iteratively review and improve their own outputs.  
    [https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-2-reflection/](https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-2-reflection/)
  - Tool Use: Leveraging code execution, web search, and APIs to make LLMs act and gather information.  
    [https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-3-tool-use/](https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-3-tool-use/)
  - Planning: Embedding explicit multi-step reasoning and planning into agent workflows.  
    [https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-4-planning/](https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-4-planning/)
  - Multi-Agent Collaboration: Designing systems of specialized LLM agents that collaborate to solve complex tasks.  
    [https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-5-multi-agent-collaboration/](https://www.deeplearning.ai/the-batch/agentic-design-patterns-part-5-multi-agent-collaboration/)

### 2. Implementation: Building Travel Planning Agents

#### a. **AutoGen Framework**
- **Design:** Implemented a travel chatbot using AutoGen as a single intelligent assistant agent, driven by GPT-3.5. The agent handled preference elicitation, recommendations, and itinerary generation in a tightly integrated sequence.
- **Flow:** The user inputs the high-level trip goals and constraints. The assistant agent autonomously follows up, gathers more details if needed, dynamically generates an optimized itinerary, and suggests activities and budgets.
- **Testing:** Ran notebook-based trials simulating user interaction for summer trip planning from Boston to Europe for four grad students on a budget.

#### b. **CrewAI Framework**
- **Design:** Designed the planning system as a multi-agent "crew," with each agent specializing in a subtask (preference gathering, destination suggestion, detailed itinerary creation).
- **Flow:** Used CrewAI’s explicit task/role decomposition: tasks are distributed among expert agents, results are sequentially passed and refined, providing greater modularity and granularity of outputs.
- **Testing:** Executed step-wise agent flows, inspecting how the intermediate outputs from each agent built collaboratively towards a final detailed itinerary.

### 3. Comparative Evaluation

Assessed both frameworks based on:
- **Quality of Output:** Depth, clarity, and personalization of generated itineraries.
- **Efficiency:** Development ease, time to production, and speed of user response.
- **Customization & Flexibility:** Ability to modify process flow or incorporate extensions (e.g., APIs, user constraints).
- **Scalability:** Suitability for handling multiple users/requests with minimal reconfigurations.
- **Ethical Considerations:** Data privacy, transparency, and risk of bias in recommendations.
- **Community & Cost:** Ecosystem maturity, documentation, and tangible costs for deployment.

### 4. Reflection & Recommendation

- Documented findings in a detailed report and compared practical experiences of both FWs, highlighting the business impact and operational nuances of each approach.[2]
- Justified the selection of a single "best fit" framework for the travel itinerary agent use-case, using the criteria above.

## Key Findings & Results

| Aspect              | AutoGen                              | CrewAI                                |
|---------------------|--------------------------------------|---------------------------------------|
| **Output Quality**  | High, consistent, streamlined.       | Thorough, modular, explicit outputs.  |
| **Efficiency**      | Rapid development & response.        | More setup effort due to agent design.|
| **Customization**   | Flexible; less decomposed.           | Highly granular; easy to extend.      |
| **Scalability**     | Handles volume with few changes.     | Potentially resource-intensive.       |
| **Ethics**          | Manages privacy easily.              | Needs care for inter-agent data.      |
| **Community/Cost**  | Active but newer.                    | Fast-growing, good docs.              |
| **Business Fit**    | Best for single-flow interactions.   | Best for tasks needing roles/approval.|

**Core Takeaways:**
- **AutoGen** performed best for rapid, user-friendly deployment, and is ideal when interactions are streamlined and resource constraints are important.
- **CrewAI** excelled in task customization and role clarity, which may be critical for more complex, regulated, or collaborative scenarios.
- Ultimately, **AutoGen was selected** as the primary tool for the main business need of fast, accurate, and flexible travel itinerary planning, with CrewAI highlighted as a solid alternative when workflows demand higher modularity or role delegation.[2]

## How to Use / Run

1. Download the relevant agent notebooks (`BA840-Team-08-AutoGen-Framework.ipynb`, `BA840-Team-08-CrewAI-Framework.ipynb`).
2. Set up required API keys and Python dependencies (see notebook cells).
3. Open notebooks in Jupyter/Colab, execute cells as directed, and follow prompts to simulate end-to-end travel planning.
4. Compare outputs and adjust task/role definitions to test extensibility.

## Requirements

- Python ≥ 3.8
- openai, crewai, autogen, langchain_community, pandas

## Learning & Takeaways

- Gained hands-on experience with both state-of-the-art single- and multi-agent LLM frameworks.
- Practiced translating business needs into operational agent architectures.
- Developed critical skills in benchmarking, ethical analysis, and making technology recommendations based on real implementation, not just theory.

## Project Details

- **Completed:** May 2024  
- **Course:** Responsible AI & Data Ethics (BA840), Boston University MSBA

*This project demonstrates the power—and tradeoffs—of agentic LLM frameworks for automating real-world business processes, and provides a template for evidence-based evaluation in future AI solution deployments.*

: Andrew Ng, DeepLearning.AI "Agentic Design Patterns" Blogs[1]
: BA840-Team-08-Travel-Itinerary-Agent-Report.pdf, Team Notebooks (AutoGen, CrewAI), Exercise Instructions.[2]
