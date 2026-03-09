---
tags:
  - concept
status: covered
---

# Agentic Workflows

> [!info] In short
> Design patterns for building AI applications that chain together multiple [[LLMs|LLM]] calls in structured sequences — plan, execute, review, iterate — instead of relying on a single prompt and response.

Think about how a restaurant kitchen works. You don't have one chef doing everything from taking the order to plating the dish. Instead, the order comes in, someone reads it and assigns tasks (routing), the prep cook chops ingredients and passes them to the line cook (chaining), the head chef oversees everything and delegates (orchestrator), and the expeditor checks every plate before it goes out (evaluator). That's basically what agentic workflows do with LLM calls — break a complex job into specialized steps and coordinate them.

When people first use ChatGPT or Claude, they think AI products work by sending one really good prompt and getting one answer back. But that's almost never how real AI applications are built. Behind the scenes, products like coding assistants, research tools, and customer support bots use carefully designed pipelines where multiple LLM calls work together, each handling a different part of the job.

There are a few core patterns worth knowing. **Prompt chaining** is the simplest — the output of one LLM call becomes the input to the next, like an assembly line. You might have one call summarize a document, a second extract key facts from that summary, and a third generate a report from those facts. **Routing** is when the system looks at incoming input and decides which specialized prompt or model to send it to — kind of like a receptionist directing your call to the right department. **Orchestrator-workers** is a pattern where one LLM acts as a manager, breaking a big task into subtasks and delegating them to worker LLMs, then combining the results. And **evaluator-optimizer** is where one LLM checks another's work and sends it back for revision if it's not good enough — basically a built-in quality control loop.

Then there are **multi-agent systems**, where you have multiple specialized [[Agents]] collaborating on a task. One agent might handle research, another does writing, a third checks for accuracy. This is one of the hottest areas in AI engineering right now, though it's still maturing and can get complex fast. The general advice is to pick the simplest workflow pattern that gets the job done — you don't always need a team of agents when a straightforward chain will do.

The important takeaway is that [[AI Engineering]] is less about crafting one perfect prompt and more about designing these workflows. How you break down a problem, which pattern you pick, what [[Tool Use|tools]] you give each step, and how you set up each [[System Prompt]] — that's where the real engineering happens.

## Related
- [[Agents]] - agents are what execute within these workflows
- [[Prompt Engineering]] - each step in a workflow needs well-crafted prompts
- [[AI Engineering]] - agentic workflows are a core part of the discipline
- [[Tool Use]] - workflows become powerful when individual steps can use external tools
- [[System Prompt]] - each LLM call in a workflow typically has its own system prompt
