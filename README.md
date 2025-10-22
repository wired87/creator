# creator


Design an AI Agent using langgraph and ray. 

needed are the followign actors:
# Relay(serve app):
Handle and clasify (use model from string with langchain) user input to keys of a dict[key, runnable_method] 
methods:
-  llm get task and extend it in detail sepparated into sub tasks
-  identify each sub task and loop though them return list of strings
-  for each identified sub task create a actor "Coder" which you provide with the exact -> save in local nx.G actor ref, sub task id 

# Coder:
identify 
  Receives a chunk of the split coder instructions.
  methods:
  pip api to receive runnable install commands jsut import install requirements
  identify package of given import statements in list[str] format
  
