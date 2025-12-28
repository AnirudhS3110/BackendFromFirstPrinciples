## API Key based Auth:
- Popular example is LLM Models API keys, eg: Gemini API key, 
- by clicking "Create Access key", the it generates a random cryptographic String.
- Using this string, we can **gain ACCESS to the Server**.

## Why use API key based Auth:
- Easy to implement.
- Ideal for Machine to Machine Communication:
- - For example we are creating an AI App to summarize topics, the Client First sends teh Question to Our Server, Our Server Communicates with the Servers in which LLMs are Depoloyed and these API Keys enable the communication between our server and the LLM's server.