# crewNER: Multi-Agent AI for Clinical NLP  

## Overview  
crewNER is a initiave that explores the use of multi-agent AI systems for Natural Language Processing (NLP) tasks, specifically focusing on Named Entity Recognition (NER) in clinical datasets. Using **crewAI**, the project leverages collaboration between specialized agents to process and annotate text efficiently.  

In its initial phase, the project focuses on implementing and testing specialized agents and a validation agent. Future iterations will expand to include a complete flow with a relevance-checking agent at the start.  

## Objectives  
The main goal is to create a modular and scalable AI system with the following agent types:  

1. **Relevance-Checking Agent**:  
   - Analyzes input text to determine if it is relevant to healthcare contexts.  
   - If relevant, forwards the text to NER agents.  
   - This agent will be implemented in later iterations.  

2. **NER Specialized Agents**:  
   - A group of agents, each responsible for tagging specific entities in the text.  
   - Example groups of tags each agent will handle:  
     - **Agent 1**: Medical conditions, symptoms, and diseases.  
     - **Agent 2**: Medications, treatments, and dosages.  
     - **Agent 3**: Anatomical locations and body systems.  
     - Additional agents can be added to scale tasks as needed.  

3. **Validation Agent**:  
   - Consolidates the output of all NER agents.  
   - Validates whether the annotations meet quality standards.  
   - If results are unsatisfactory, it can request a single re-analysis from the appropriate NER agent.  
   - Returns unified and formatted responses.  

## Implementation Phases  
### Phase 1:  
- Implement the **NER Specialized Agents** and the **Validation Agent**.  
- Use **OpenAI** models to power the agents.  

### Phase 2:  
- Introduce the **Relevance-Checking Agent** to create a complete flow.  
- Implement the logic to execute NER tasks only if the text is deemed relevant.  

### Phase 3:  
- Transition from OpenAI models to **Ollama**, leveraging **gemma2:27b-instruct-q4_0** for improved performance and control.  

## Technologies Used  
- **crewAI**: Framework for orchestrating multi-agent systems.  
- **OpenAI**: World-clas LLM model for generative models. (It will be used to generate in the first version of the project)
- **Gemma2**: A high-performing and efficient model available in three sizes: 2B, 9B, and 27B.
- **Ollama**: It provides a simple API for creating, running, and managing models, as well as a library of pre-built models that can be easily used in a variety of use cases.  
- **Python**: Core language for development.  

## Future Directions  
- Expand the system to support additional NER tasks and entity types.  
- Experiment with alternative LLMs for cost efficiency and performance improvements.  
- Benchmark multi-agent architectures for clinical NLP tasks to evaluate scalability and real-world applicability. 

## Contributing  
Contributions and ideas are welcome! Feel free to open issues or submit pull requests to help improve the project.
