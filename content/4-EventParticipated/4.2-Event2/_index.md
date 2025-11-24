---
title: "Event 2"
date: 2025-09-07
weight: 1
chapter: false
pre: " <b> 4.2. </b> "
---


# Summary Report: “Generative AI with Amazon Bedrock”

### Event Objectives

- Learn what Amazon Bedrock is and how many model that AI used
- Learn more Prompting Engineering like: Zero-Shot, Few-Shot, Chain of Thought(CoT)
- Learn what Retrieval Augmented Generation is and RAG use cases
- More pretrained AI Services
- Learn what Amazon Bedrock agent core and demo
### Speakers

- **Lam Tuan Kiet** – Sr DevOps Engineer, FPT Software
- **Danh Hoang Hieu Nghi** – AI Engineer, Renova Cloud
- **Dinh Le Hoang Anh** – Cloud Engineer Trainee, First Cloud  AI Journey

### Key Highlights
- **Foundation Models**
- **Prompt Engineering**
- **Retrieval-Augmented Generation(RAG)**
- **Bedrock AgentCore**

#### Foundation Models
![Why foundation models](/images/foundation_model.jpg)

| | Tradional ML models| Foundation models|
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------- |
| Purpose| Narrow, task-specific(Classification, regression,forecasting,clustering,etc...)|General-purpose, multi-domain, multi-task  |      |
| Training data| Usually structured/tabular or domain-specific|Massive datasets (text, images, code, etc.)|||
| Training required   | Must be trained manually using labeled data |None — already pretrained|      |  |
| Customization   | You need to adjust hyperparameters, features, datasets|Optional — fine-tuning, RAG, prompt engineering |   |  |
| Example   | Random Forest, XGBoost, SVM, Linear Regression|Claude, Llama, Cohere Command, Titan |      |  |
|Skill Needed|High ML expertise (feature engineering, training pipelines)|Very low — prompt-based usage|||
|AWS Services|**SageMaker**, Amazon ML, custom training|Amazon Bedrock, Bedrock Studio|||
|Use cases|Predicting, Forecasting sales, Classifying images, Fraud training, Anomaly detection| Chatbots, Text summarization, Code generation, Image generation, Conversational apps, Document search with RAG, Sentiment analysis, Multi-language translation|||

Supported foundation models in Amazon Bedrock
![Supported foundation models in Amazon Bedrock](/images/supported_foundation.jpg)

#### Prompt Engineering - Crafting and refining instructions(prompts)
#### What is a prompt?
- Is the input you give to an AI model (like ChatGPT, Claude, Gemini, or models on Amazon Bedrock) to get a specific output.
#### Example
![Example](/images/example_prompt.jpg)

#### What is difference between Zero-Shot, Few-Shot and Chain of Thought in Prompting Techniques?

| Technique            | Description                                                | When to Use                                      | Advantages                                         | Limitations                                         | Example Prompt Style                          |
|----------------------|------------------------------------------------------------|--------------------------------------------------|----------------------------------------------------|-----------------------------------------------------|-----------------------------------------------|
| **Zero-Shot**        | Model gets only the instruction with **no examples**.      | Simple tasks; model already understands domain.  | Short prompts, fast, minimal setup.                | Lower accuracy for complex or domain-specific tasks.| "Classify the text into neutral, negative or positive" |
| **Few-Shot**         | Provide **a few examples** to teach the pattern.           | Custom formats; domain tasks; pattern learning.  | Higher accuracy; model learns your desired style.  | Longer prompt; can become costly at scale.          | "A whatpu is a small, furry animal native to Tanzania. An example of a sentence that uses the word whatpu is: <br>We were traveling in Africa and we saw these very cute whatpus. " |
| **Chain-of-Thought** | Ask model to **explain reasoning step-by-step**.           | Math, logic, coding, planning, reasoning tasks.  | Better reasoning, more accurate complex outputs.   | Slower; may generate unnecessarily long answers.    | "Show your step-by-step reasoning."           |



#### Retrieval Augmented Generation (RAG)- Retrieving relevant information from a data source
#### What is Retrieval Augmented Generation?


- **Retrieval**: Fetches the relevant content from the external knowledge base or data sources based on a user query 
- **Augmentation**: Adding the retrieved relevant context to the user prompt, which goes as an input to the foundation model  
- **Generation**: Response from the foundation model based on the augmented prompt
#### RAG Use cases
- **Improved content quality**: E.g Helps in reducing hallucinations and connecting with recent knowledge including enterprise data
- **Contextual chatbots and question answering**: E.g Enhance chatbot capabilities by integrating with real-time data
- **Personalized search**: E.g Searching based on user previous search history and persona
- **Real-time data summarization**: E.g Retrieving and summarizing transactional data from databases, or API calls   
![RAG](/images/RAG.jpg)
#### What are embeddings?

- Numerical representation of text(vectors) that captures semantics and relationships between words
- Embedding models capture features and nuances of the text
- Rich embeddings can be used to compare text similarity
- Multilingual Text Embeddings can identity meaning in different languages

- **Amazon Titan Embedding**:<br>&emsp;
    + **Titan Text Embeddings**: Translates text inputs(words,phrases) into numerical representations(Embeddings). Comparing embeddings produces more relevant and contextual responses that word matching
    + **Highlights**:<br>&emsp;
        + Amazon Titan Text Embeddings V2 is a light weight, efficient model ideal for high accuracy retrieval tasks at different dimensions.
        + The model supports flexible embeddings sizes and prioritizes accuracy maintenance at smaller dimension sizes.
        + Support for 100+ language in pre-training as well unit vector normalization for improving accuracy of measuring vector similarity. 

![Amazon Titan Embedding](/images/amazon_titan.jpg)
 **RAG in Action**
![Amazon in Action](/images/RAG_Action.jpg)

**Data Ingestion Workflow**
![Amazon ingestin workflows](/images/ingestion.jpg)

**RetrieveAndGenerate API**

![RetrieveAndGenerate API](/images/retrieveAPI.jpg)

#### Other Pretrained AI Services

![Amazon translate](/images/z7226100700576_8c6d6f4fb782f49cefb3ad8c11c77db2.jpg)

![Amazon Textract](/images/z7226100718462_385f2bde80fcd61d9e5ee0d6b7732f89.jpg)

![Amazon transcribe](/images/z7226100740453_ea3987164a7d69381c4e298f2e847a9b.jpg)
(hinh anh amazon polly)
![Amazon Polly](/images/z7226100772259_db269fba041e5507e412175ec3a85b34.jpg)
(hinh anh amazon comprehend)
![Amazon Comprehend](/images/z7226100734521_f068686a3d3c479dc00272d1eb50ad55.jpg)
(hinh anh amazon kendra)
![Amazon Kendra](/images/z7226100721932_43e82f26dd0532d8525087fd96929c74.jpg)
(hinh anh amazon lookout family)
![Amazon Lookout Family](/images/z7226100739536_2c2b097cf02df57d39fe18d3e11318c0.jpg)
(hinh anh amazon personalize)
![Amazon personalize](/images/z7226100780833_f24a38ebe15aa1e900bcaae88aa94538.jpg)


### Amazon Bedrock AgentCore

#### The evolution into Agentic

- **Generative AI assistants**: Follow a set of rules, Automate repetitive tasks  
- **Generative AI agents**: Achieve a singular goal, address broader range of tasks, automate entire workflows  
- **Agentic AI systems**: Fully autonomous, multi-agent systems, mimic human logic and reasoning

#### Frameworks for building agents

- **Strands agents SDK**  
- **Langgraph, langchain**  
- **OpenAi Agents SDK** 
- **Crew.AI** 
- **Google ADK**
- **Llamaindex**

#### The protype to production "chasm"

![protype](/images/z7226100812733_a380cf409ce7a61e17eb568bf9305dd3.jpg)
- **Phased approach**: No rushing — follow a clear roadmap  
- **7Rs framework**: Multiple modernization paths depending on the application  
- **ROI measurement**: Cost reduction + business agility  

### Getting agents to productions in still too hard

- **Securely execute and scale agent code** 
- **Remember past interaction + learning**
- **Identity and access controls for all agents and tools** 
- **Agentic tool use for executing complex workflows**
- **Discover and connect with custom tools and resources**  
- **Understand and audit every interaction**
![productions](/images/z7226100809106_419bcc96e0e9869e70bfc1ee204c68d5.jpg)


### Agent core services enabling agents at scale

![Agent scale](/images/z7226100823612_1879c44a5cfd3d4dc19e10c65af04445.jpg)
### Event Experience

Attending the **“Generative AI with Amazon Bedrock”** workshop was a highly valuable experience, giving me a comprehensive understanding of how modern AI and cloud technologies are applied in real-world scenarios. The event combined expert insights, hands-on demonstrations, and practical guidance that helped connect theory with implementation.

#### Learning from industry experts
- Speakers from AWS, Renova Cloud, and FPT Software shared **real-world best practices** for AI adoption and cloud modernization.  
- Their case studies demonstrated how organizations apply **foundation models, RAG, and agent-based architectures** in enterprise systems.  
- The discussions helped clarify not just how these technologies work, but **why they matter** for scalability and business innovation.

#### Hands-on technical exposure
- Practical sessions on **Zero-Shot, Few-Shot, and Chain-of-Thought** prompting improved my understanding of effective prompt engineering.  
- The walkthrough of **RAG workflows** showed how grounding AI responses in real data reduces hallucinations and improves accuracy.  
- Live demos of **Bedrock AgentCore** helped me visualize how AI agents plan tasks, execute tools, and integrate securely with AWS services.

#### Understanding modernization and architecture
- The workshop highlighted the shift from traditional ML to **foundation-model-driven AI** and explained the differences in training, customization, and usage.  
- I learned how organizations modernize systems using:
  - **Event-driven architecture**
  - **Domain-driven design (DDD)**
  - **AI-augmented workflows**
- These approaches helped me understand how to design applications that are **scalable, resilient, and intelligent**.

#### Exposure to modern AI tools
- Demonstrations of **Amazon Titan Embeddings**, **Textract**, **Comprehend**, **Kendra**, **Polly**, and other AI services showed how to quickly integrate intelligence into applications.  
- Learning about **Amazon Q Developer** highlighted how AI can support the entire software lifecycle—from planning to coding and refactoring.

#### Networking and knowledge exchange
- Discussions with cloud engineers, AI specialists, and developers broadened my understanding of industry use cases and challenges.  
- These conversations reinforced the importance of aligning **business objectives**, **data modeling**, and **technology decisions**.

#### Key takeaways
- **RAG** enables enterprise-grade AI by grounding answers in verified data.  
- **Prompt engineering matters**—well-structured prompts lead to more reliable results.  
- **Agentic AI systems** represent the next evolution of automation, capable of reasoning and executing multi-step workflows.  
- System modernization requires a **phased roadmap** and clear ROI measurement.  
- Integrating AI tools into the developer workflow can significantly **boost productivity** and reduce operational overhead.

