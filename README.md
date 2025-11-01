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

---
## Learnings from Module 1 (Lec 5) Agent-with-memory.ipynb
- I learnt how to add memory to agents using the concept of threads and Memory() function using langgraph. Passing the same thread_id lets us proceed from the previous checkpoint.
  
- I ran the code using my own example by using the calculator tool from the previous file and used memory successfully by passing in the thread id.

- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/agent-memory.ipynb





---
## Learnings from Module 2 (Lec 1) State-schema.ipynb
- I learnt how to use different types of ways of defining the state schema for my graph. The different types are TypedDict class, or Dataclass(use state.name instead of state['name'])
and Pydantic, which is great for data validation.
  
- I ran the code and tried out my own example to choose from 2 different numbers using all the three state schema defining methods.

- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/state-schema.ipynb

---
## Learnings from Module 2 (Lec 2) State-reducers.ipynb
- I learnt about the working of state reducers, which control how state updates are handled when multiple nodes modify the same state key at the same time. I also learnt about built-in reducers like add and add_messages and how to create custom reducers to handle edge cases.
  
- I ran the code and made my own example which ahs the functionality to add words instead of incrementing a number. Made my own custom reducer to handle None inputs and implemented RemoveMessage for the same example


- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/state-reducers.ipynb


---
## Learnings from Module 3 (Lec 1) Streaming-interruption.ipynb
- I learnt how to use and implement different streaming modes in langgraph - full state values, state updates, and individual tokens. I also learnt how to visualize graph execution in real-time using various streaming methods.
  
- I ran the code and tried out my own example which implements a simpler chatbot and showed the different ways of streaming. Example streaming only tokens
<img width="1288" height="576" alt="Screenshot 2025-10-27 at 8 43 25 PM" src="https://github.com/user-attachments/assets/b3c7abf7-db7d-47c5-8b9a-b973e4524af8" />


- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/streaming_interruption.ipynb

---
## Learnings from Module 3 (Lec 2) Breakpoints.ipynb
- I learnt how to use breakpoints. They allow you to pause graph execution at specific nodes, enabling human-in-the-loop workflows like approval and debugging.
  
- I ran the code and made a math assistant that squares, cubes, and doubles numbers, using breakpoints to pause before tool execution so users can approve or cancel calculations.

- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/breakpoints.ipynb

---
## Learnings from Module 3 (Lec 3) edit-state-human-feedback.ipynb
- I learnt how to edit graph state during interruptions and add human feedback nodes. This allows for user input mid execution and real-time modification of agent behaviour.
  
- I ran the code and used the math assistant from the previous file and demonstrated how to edit state by modifying user requests mid-flow and adding human feedback nodes to intercept and alter calculations.
  
- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/edit_state_human_feedback.ipynb

---
## Learnings from Module 3 (Lec 4) dynamic-breakpoints.ipynb
- I learned how to use dynamic breakpoints with NodeInterrupt to conditionally stop graph execution based on runtime conditions. The example showed how to interrupt when input length exceeds a limit, then update state and resume execution.
  
- I created a simpler number checking example that interrupts when a number is greater than 10. The new example uses basic number comparison instead of string length checks, making it easier to understand while demonstrating the same dynamic breakpoint concept.
  
- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/dynamic_breakpoints.ipynb

---
## Learnings from Module 3 (Lec 5) time-travel.ipynb
- I learned how to implement "time travel" debugging in LangGraph, which allows viewing, replaying, and forking from past states of an agent's execution. This enables powerful debugging capabilities as it lets me inspect historical states, re-run from any checkpoint, and create alternative execution paths by modifying state at specific points.
  
- I ran the code and made my own example with tools such as square cube and double and updated all the example queries to use these new operations. The examples now demonstrate chaining operations like "calculate the square of 5 and then double the result" instead of simple multiplication problems.
  
- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/time_travel.ipynb


---
## Learnings from Module 4 (Lec 1) parallelization.ipynb
- I learnt the working of parallel node execution in langgraph and how to create simple fan-out and fan-in programs. I learnt thhe use of reducers like operator.add in handling concurrent updates from parallel paths in the same graph or ensuring nodes to write separate state keys to avoid errors.
  
- The calculator example demonstrates this parallel execution by taking a single input value and simultaneously calculating a sum and a product (the fan-out). The graph waits for both parallel operations to complete, and a final answer node combines both unique results to output the complete set of calculated values (the fan-in).
  
- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/parallelization.ipynb

---
## Learnings from Module 4 (Lec 2) sub_graphs.ipynb
- I learnt about the use of sub graphs to structure complex graphs into parallel execution of multiple tasks. The parent and sub-graphs communicate using overlapping keys and parallel outputs are merged using the add reducer to combine lists.
  
- My RecipeManager class takes a recipe and runs two subgraphs in parallel, one to calculate the ingredient cost and the other for nutritional analysis. The parent graph combines the outputs of both the graphs into a single final result

- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/sub_graph.ipynb

---
## Learnings from Module 4 (Lec 3) map_reduce.ipynb
- I learnt about the Map-reduce pattern in langgraph. The map phase involves using Send to decompose and parallelize a task and the reduce phase involves priocessing the outputs from all the parallel outputs. The we can use Annotated[list, operator.add] in the OverallState as usual.
  
- The example I used here involves the LLM to generate three different taglines using Map and then Reduce to compare the the taglines and decide which one is best(According to the criteria of the shortest winning). 

- https://github.com/adi230306/aditya-singh-langgraph-mat496/blob/main/map_reduce.ipynb
