# aditya-singh-langgraph-mat496

---
## Learnings from Module 1 (Lec 1) Simple_graphs.ipynb
- I learnt how to make nodes, edges(as functions) and build a simple graph using StateGraph. I also learnt how too display said graph using in-built functions and how to invoke the graphs
  
- I implemented a simple graph which prints wether I passed my exam or failed it on a 50/50 chance.<img width="275" height="331" alt="Screenshot 2025-10-16 at 7 13 13 PM" src="https://github.com/user-attachments/assets/dc41058c-6ed4-48b2-8fca-8926a0933529" />
- Link to file: https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/simple-graph.ipynb

---
## Learnings from Module 1 (Lec 2) Chain.ipynb
- I learnt how to make chains using langgraph where we can pass in chat messages(AIMessages, HumanMessages) as the graph state, chat models as the graph node and also revised how to use tool calls by binding them wih the chat models.
  
- I ran the code using my own example by asking the model about Attack on Titan.
  
- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/chain.ipynb

---
## Learnings from Module 1 (Lec 3) Router.ipynb
- I learnt how to make a basic router where the llm model takes a call wether to route the answer to an llm-based response or using a tool call. Learnt the use of ToolNode and tools_condition to make tool calling easier.
  
- I ran the code using my own example by making a router that decides wether to use a tool that calculates the factorial of a function or not.
<img width="1440" height="788" alt="Screenshot 2025-10-16 at 8 57 54 PM" src="https://github.com/user-attachments/assets/bfe73e58-637f-4c54-b966-08a86ba7d803" />
(frontend testing for the above-mentioned tool)
-Link: - https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/router.ipynb


---
## Learnings from Module 1 (Lec 4) Agents.ipynb
- I learnt how to make a basic agent in langgraph by passing the output of the tool calling node in the graph back to the llm to finally generate an llm-based response to the END edge
  
- I made a calculator tool calling node which includes a list of 4 tools: add, multiply, divide and factorial. The output of this node was fed back into the llm to generate a llm-response and create an agent. The following are the screenshots of my prompt aand what tools were called finally:
<img width="747" height="26" alt="Screenshot 2025-10-16 at 9 21 54 PM" src="https://github.com/user-attachments/assets/1e31b9ab-806c-42c2-ad13-90af1c989630" />
<img width="591" height="544" alt="Screenshot 2025-10-16 at 9 22 24 PM" src="https://github.com/user-attachments/assets/1c90bce1-2fc8-4541-b6f2-f80d6f5a413c" />
<img width="219" height="251" alt="Screenshot 2025-10-16 at 9 22 44 PM" src="https://github.com/user-attachments/assets/762624d0-4abd-4e97-a258-82317ceffa9a" />

- Link: - https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/agent.ipynb
