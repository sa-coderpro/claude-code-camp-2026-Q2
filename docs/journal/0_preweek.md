## Preweek Technical Documentation

## Technical Goal
The techincial goal of Preweek Explore is to determine how well do Agent architecture is going to fit in business use-case.

Examples of Agent Architectures that scale with effort:
 - An agent file with referenced files eg. AGENT.md, @~/docs/*.md
 - Agent skills driven by main agent.
 - Filesystem subagents driven by a coding harnesses
 - AI workflow automation platform like n8n
 - Generic AI Agents SDK can be leveraged to explore AI packages
 - Use low cost LLM Agents and write own agentic loop to explore
 - Use REST APIs directly, while writing the Agentic Loop code
   - Agentic loops are model driven orchestration with middle programmatic guidance
   - Agentic loop is code driven orchestration.

## Technical Uncertainity
- I am not sure if an coding harness agentic loop will be effective/productive to drive non coding workload
- Not sure LLD Models thinking mode is sufficient enough to hold memory and drive decision in our task.
- Not sure coding harnesses can interact with MUD without an interface or SDK or manage telenet sessions.

## Technical Hypothesis
- We might need an interface since long live telenet session management is pretty hard.
- We might need to roll out our own agent without an SDK because generic primitives for observability, memory management and usage requires specialized implementation.

## Technical Observations
- An Agent.md file could not connect to MUD, it could produces scripts but it was unreliable in creating connection to MUD and needed knowledge of deterministic TUI of MUD.
- Skills and Sugagents performed accompained with a script to manage the telenet session. They were able to play the MUD, but may be not efficiently.
- Using markdown files where the coding harnesses updates it as simple memory was not effective as it was trying to store brittle navigational path , may be knowledge base graph database will be better.

## Technical Conclusion

- Skills and subagents are capable of driving the MUD.
- We do not need specialized memory for map navigation and world data 
- We opened a new technical use case of if we should have our own agent to handle multiple sessions of multiple players, playing at same time since co-op its common factoe in MUDs which we forget to consider in our design.
- We could not explore n8n completely due to technical restraints executing external scripts
- Implementing our own speicalized agentic loops remain technical uncertain and will need explored in depth in week 2.
- Without a customized agentic loop the agents could not perform goals effeciently 

## Key Takeaways
When we have a specialized use case like a playing MUD, we cannot leverage generic SDKs for Agents, we need specialized tools and agentic loops.