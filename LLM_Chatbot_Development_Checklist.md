# **AI Application Development Checklist For Beginners**

By Cameron Williams 1/2/2026

This checklist/guide should not be treated as a concrete rule book for how to create AI applications, instead it should be a general guide to help you understand whats needed and what to think about as you are engineering your AI application. 

Overall, I expect the developer to continue exploring and finding new ways not listed in the guide for engineering applications that use AI technology. 

1\. Define the Use Case

- [ ]  Clear problem statement  
- [ ]  Target users  
- [ ]  Read-only vs action-based

2\. Data Assessment

- [ ] Data sources identified  
- [ ] Data structure evaluated  
- [ ] Frequency of data updates defined (optional)  
- [ ] Data usage meets compliance requirements (If needed)

3\. Prompting vs Fine-Tuning

* Prompt-only strategy validated (depending on use case, preferably you will want to stick with one option below. On occasion you may have to mix different prompting techniques if you are using different agents within one AI application/product)  
- [ ] Zero-Shot Prompting \- Giving clear instructions to the model with little to no examples.   
- [ ] Few-Shot Prompting \- You give the model multiple examples of what good outputs are.  
- [ ] Chain-of-Thought / Structured Prompting \- You provided a structured method for how the model should think when approaching problems or when interacting with users.   
* Is Fine-tuning criteria needed?   
- [ ] Full Fine-Tuning \- This can be costly and extremely time consuming but can alter how the model behaves for the benefit of creating a highly specialized product for specific domains as needed.   
- [ ] Parameter-Efficient Fine-Tuning (PEFT / LoRA) \- This option is cheaper and faster than full fine tuning. This is what most companies choose to do due to it being a reasonable option compared to full tine tuning. Use this when you don't necessarily need serious specialization but instead you need a consistent tone and behavior.   
- [ ] Instruction / Supervised Fine-Tuning (SFT) \- You train the model on specific input and output pairs. Rather than just teaching the model specific knowledge you are also teaching the model how to behave, this can be a more robust way of PEFT / LoRA. You can perform this training on the OpenAI platform.   
- [ ] Training and evaluation datasets prepared

4\. LLM/SLM Selection

- [ ] Primary model chosen and why?  
- [ ] Fallback model identified and why? (If primary model results lack.)  
- [ ] Cost and latency benchmarks evaluated

5\. Retrieval Strategy (Please use this only if you plan to use documentation and routing in your AI product, if not, please skip)

- [ ] \- RAG or CRAG selected  
- [ ] \- Chunking and metadata strategy defined  
- [ ] \- Query routing logic implemented

6\. Vector Database & Embeddings (Please use this only if you plan to use documentation and routing in your AI product, if not, please skip)

- [ ] \- Embedding model selected  
- [ ] \- Similarity metric chosen  
- [ ] \- Namespace and update strategy defined

7\. Framework & Orchestration

- [ ] Prompt templates versioned \- You have the ability to interchange prompts if needed and keep track of changes (especially needed for prod environments)  
- [ ] Tool calling isolated \- Tools should be defined outside the AI app itself as a best practice. Tools can be APIs, functions, triggers, etc. that are used by the application to complete tasks.  
- [ ] Memory management defined \- Do past conversations matter? Should the memory be short term or long term? How long are conversations retained or will they be archived? 

