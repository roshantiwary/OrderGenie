# OrderGenie with LangGraph and the Gemini API

In this notebook, you will use [LangGraph](https://www.langchain.com/langgraph) to define a stateful graph-based application built on top of the Gemini API.

You will build a simulated retail User Account Management system, called OrderGenie. It will provide a looping chat interface to customers where they can query about order history and order status and also make order cancellations and initiate returns

OrderGenie is used in other Gemini API demos, so if you are looking to explore something with a more minimal implementation, check out the [EcomAccountBot function calling example]() that implements a similar system using only the Gemini API Python SDK and function calling.

# Building a Gemini Langgraph AI Agent: A Comprehensive Guide
In the ever-evolving world of AI-driven solutions, integrating diverse capabilities of generative AI into a cohesive system can significantly enhance functionality and user experience. This guide explores the development of a Gemini Langgraph-based AI agent, designed to manage and process customer orders with advanced AI features such as structured output, few-shot prompting, grounding, and more. Let's embark on the journey of building this intelligent assistant.

# Introduction to the AI Agent
        Our AI agent, OrderGenie, serves as an interactive chatbot that helps users manage their orders by interfacing with a SQL database. Using LangGraph and Gemini, the agent efficiently interacts with users, providing purchase histories, managing returns, and handling cancellations—all while ensuring data privacy and accuracy.

# Key AI Capabilities Integrated
* **Structured Output**: The agent utilizes structured output to perform specific functions, such as invoking database query tools via predefined interfaces.This enhances clarity and consistency in the user's interaction with the AI, ensuring that the output is predictable and well-organized, especially when displaying order details or transaction summaries.
* **Function Calling**: By leveraging decorated Python functions, the agent invokes precise operations like listing tables, describing schemas, and executing queries. Function calling modularizes the operations, ensuring dependable interactions with the database. This abstraction allows the AI to handle complex tasks efficiently while presenting a simple interface to the user.
* **Controlled Generation**: The AI is trained to follow given instructions, keeping conversations focused and directed toward specific outcomes, like querying order details. Controlled generation maintains the relevance and coherence of interactions, which is crucial for professional and accurate customer service engagements, preventing deviations into unrelated topics.
* **Agents**: OrderGenie functions as a self-contained agent, autonomously managing conversation flow and task execution without needing external prompts. This autonomy enables the AI to streamline operations by handling routine tasks, reducing the need for human oversight and increasing service scalability.
* **Few-shot Prompting**: The agent is guided using a few examples included in the instructions, showing typical user interactions to guide response generation. Few-shot prompting equips the AI with the ability to respond appropriately to similar scenarios, enhancing its adaptability and accuracy even when encountering limited data.
* **Grounding**: The AI ensures its responses are based on factual data from the database, validating information before presenting it to the user. Grounding enhances the credibility of responses by tying them to verifiable data, reducing errors, and building user trust.

## **IMPORTANT!**

The app built in this notebook takes **user input** using a **text box** ([Python's `input`](https://docs.python.org/3/library/functions.html#input)). These are commented-out to ensure that you can use the `Run all` feature without interruption. Keep an eye out for the steps where you need to uncomment the `.invoke(...)` calls in order to interact with the app.

If you wish to save a version of this notebook with `Save and Run all`, you will need to **re-comment** the lines you commented-out to ensure that the notebook can run without human input.
