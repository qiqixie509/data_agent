# data_agent
This is a multi-agent system that can perform web research, answer questions and generate charts, integrated with Snowflake Cortex Agents for grounded data and private data access.

## Environment
LangChain: Planner, Executor, Web Researcher, Chart Generator, Chart Summarizer, Synthesizer      
Snowflake: Provide grounded data for the cortex researcher       
Trulens: an open-source library designed for evaluating and tracking LLM applications, particularly those built with RAG and agentic workflows.         

``` bash
# install dependencies
pip install -r requirements.txt
```

## Multi-Agent System

### Architecture
![architecture](pictures/architecture.png)

### Components
- Planner
- Executor
- Web Researcher
- Cortex Researcher
- Chart Generator
- Chart Summarizer
- Synthesizer

## Add Cortex Researcher
### Architecture
![cortex_architecture](pictures/cortex_architecture.png)

### New Components
- Cortex Researcher

## Observe Agent Perforrmance
Because the data agents at their core are performing research and generation tasks, we can apply the RAG Triad to assess the data agent's goal completion.

### RAG Triad
- Answer Relevance
- Context Relevance
- Groundedness
![rag_triad](pictures/rag_triad.png)

### OpenTelemetry traces and evaluations


## Measure Agent's GPA
Agents are most effective when acting in alignment with a high-quality plan. For that reason, we can identify common failure modes stemming from misalignment between the goal, the plan and the agent's actions. Then through careful criteria and a strong LLM judge, we can develop evaluators to detect these common agent failure modes and assess separable dimensions of agent quality.


