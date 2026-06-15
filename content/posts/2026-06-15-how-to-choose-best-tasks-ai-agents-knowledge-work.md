+++
title = "How to Choose the Best Tasks for AI Agents in Knowledge Work"
date = 2026-06-15T09:00:00-03:00
draft = false
summary = "Why AI agents work so well for software engineering, and how to choose the right knowledge-work tasks for agentic automation."
tags = ["AI", "AI agents", "knowledge work", "enterprise AI", "automation"]
topics = ["AI"]
+++

*Versão em português: [Como escolher as melhores tarefas para agentes de IA no trabalho de conhecimento](/gabriel-dornella-blog/posts/2026-06-15-como-escolher-melhores-tarefas-agentes-ia-trabalho-conhecimento/).* 

Why do AI agents work so well for coding tasks, but still face challenges in other areas?

In my previous article, I wrote about the productivity gains developers are seeing by adopting AI for coding — especially AI agents — and how we can apply the same logic to other types of work, as long as we create the right environment for both humans and agents.

In recent weeks, two of the most innovative builders in this new wave, Peter Steinberger, creator of OpenClaw, and Boris Cherny, creator of Claude Code, took this concept one step further. They said they no longer write prompts directly for their agents. Instead, they write loops that generate prompts and interact with the agents. These loops are processes that provide context, receive responses, verify results, and continue moving forward.

That represents a massive gain in productivity and scale, because they are no longer the bottleneck in the process of writing each prompt. The implication of this new architecture is that agents can operate with more autonomy inside the right environment to execute their tasks: systems composed of loops, tools, context, validation, and agents working through increasingly long and autonomous cycles.

In software development, this is already producing significant gains. The question that interests me is: how can we apply the same logic to knowledge work in other areas of the company?

The short answer is that we can. But we cannot simply copy the model used by software engineers. The environment is different, the risks are different, and the way we choose use cases needs to be more deliberate.

## Why AI agents work so well for software

Before thinking about marketing, finance, HR, or operations, it is worth understanding why agents work so well for software development.

The first point is that code is a very natural language for LLMs. It is text. It has structure, patterns, explicit dependencies, and it can be read, written, compared, refactored, and analyzed by the agent itself. The artifact the human works with is the same artifact the agent can manipulate.

The second point is that the software environment provides fast and objective feedback. A test passes or fails. An application compiles or breaks. An endpoint returns the expected result or it does not. An error appears in a log. A visual component can be compared against a reference.

This creates powerful learning cycles. The agent does not depend only on someone's opinion to know whether it is making progress. It can take an action, observe the result, correct course, and try again.

There is also a relatively clear notion of completion. In many programming tasks, it is possible to verify whether the work was done: the bug was reproduced and fixed, the tests passed, the endpoint responded correctly, performance improved, or the interface matched the expected result.

Software agents also have access to powerful tools. They can read files, edit code, run commands, search the repository, call APIs, open pull requests, and run tests. The full context of the work is often available inside the environment itself: source code, documentation, tests, logs, configurations, issues, and Git history.

And perhaps most importantly, experimentation is relatively safe.

Git, branches, diffs, pull requests, code review, and rollback create a layer of control. The agent can propose changes, but those changes are visible. Humans can review them. Tests can validate them. If something goes wrong, it is possible to revert.

In other words, agents work well for code because they operate in an environment with four very strong characteristics:

**broad context + broad tool access + reversible actions + objective verification.**

![Why software engineering is agent-friendly](/gabriel-dornella-blog/images/posts/ai-agents-knowledge-work/software-engineering-agent-friendly-en.jpg)

This combination is what makes software development one of the best environments for AI agents today.

## The problem with applying the same logic to knowledge work

When we move away from software and look at other areas of the company, these conditions start to disappear.

Think about marketing, finance, HR, operations, or sales. These areas also perform intellectual work, make decisions, produce documents, analyze information, and coordinate processes. In theory, they seem like strong candidates for AI agents.

But the environment where this work happens is much less structured.

Business language is not always native to the models. Some information lives in text, but a lot of it exists in presentations, spreadsheets, flows, dashboards, conversations, meetings, images, diagrams, and tacit knowledge held by people. The agent may be able to read some of these artifacts, but it rarely understands the full context just by looking at the available files.

Feedback also tends to be slower and more subjective. How do you know whether a campaign brief is truly good before creative teams use it? How do you know whether a financial analysis captured all the nuances of a negotiation? How do you know whether a dashboard answers the right questions before it is used in an executive meeting?

In many cases, “done” is not easy to verify. A document may be complete, but incomplete from a business perspective. A recommendation may be well written, but wrong for the context. A decision may look reasonable today and only reveal its impact weeks later.

There is also the problem of tools. Knowledge work happens across many systems: CRM, ERP, workflow tools, email, messaging apps, documents, spreadsheets, presentations, and internal systems. Even when these tools have APIs, connecting them in a way that is safe and useful requires a consistent data model, proper permissions, and a clear understanding of the process.

Access is another issue that cannot be treated as a detail. An HR agent may have access to sensitive employee data. A finance agent may access cash flow, margin, credit, or salary information. A sales agent may see strategic negotiations. Giving autonomy without carefully designing the boundaries can create meaningful risks.

Finally, most business workflows do not have the equivalent of Git. An approved campaign does not live in a branch. A commercial negotiation does not have a simple rollback. A weak brief can create wasted work across multiple teams. A poor financial decision can affect cash flow, margin, or customer relationships.

This does not mean AI agents do not work for knowledge work. It means we need to be more careful about where we use them.

## Agents execute tasks, not entire jobs

A common mistake is to imagine that an AI agent should take over an entire job. “Let's create a marketing agent.” “Let's create a finance agent.” “Let's create an HR agent.”

That way of thinking is too broad for the current stage of the technology. Agents are much more useful when we think about specific tasks inside a larger job.

Marketing's job, for example, can be described as creating and capturing qualified demand. But that breaks down into several smaller jobs: creating campaigns, strengthening positioning, accelerating sales cycles, segmenting customers, producing creative assets, analyzing performance, and so on.

Each of those smaller jobs contains tasks: writing a brief, researching references, defining messaging, building a segmentation, reviewing assets, consolidating results, preparing a presentation.

The same logic applies to finance. Finance's job may be to ensure that financial resources are allocated, protected, and optimized to sustain growth, profitability, and predictability. But that work includes very different tasks: analyzing cash flow, reviewing commercial exceptions, approving special conditions, consolidating data, tracking indicators, preparing scenarios, and supporting decisions.

The right question is not “which area can we automate with agents?”. The right question is: “which tasks inside this area have the conditions required for an agent to operate with autonomy?”.

## A simple method for choosing good use cases

To choose where to apply AI agents in knowledge work, I would start with the area's job to be done and then break that work down into tasks.

From there, I would evaluate each task with seven questions:

1. Is the language of this task natural for the agent?
2. Is it possible to provide immediate feedback on the quality of what is being produced?
3. Is it possible to verify whether the task has been completed?
4. Are the necessary tools available to the agent?
5. Is all the necessary context available?
6. Can the agent access the necessary information, or are there special controls?
7. Is it possible to undo, review, or correct what the agent has done?

![Methodology for defining AI agents](/gabriel-dornella-blog/images/posts/ai-agents-knowledge-work/methodology-defining-ai-agents-en.jpg)

These questions help separate tasks where the agent can have more autonomy from tasks where it should act only as support for a human.

The goal is not to find tasks with no risk. That probably does not exist. The goal is to find tasks where the risk is understandable, the context is sufficient, the result is verifiable, and the scope can be expanded safely.

## Two examples: campaign brief and financial approval

Imagine two different tasks.

The first is creating a marketing campaign brief. The agent's mission would be to produce a complete document to guide creative, communications, media, and other teams involved in executing the campaign.

The second is approving a special payment condition for a customer. The agent's mission would be to evaluate an exception requested by the sales team, considering financial impact, risk, cash flow, and the probability of closing the deal.

Both tasks are important. Both involve text, analysis, and decision-making. But they do not have the same autonomy profile.

In the campaign brief case, the language is mostly text. The agent can work with templates, campaign history, brand documentation, positioning, product characteristics, and information about the audience. It is possible to compare the brief produced against an expected model. Another LLM or review process can assess whether the document is complete, clear, and aligned with the objective.

Completion is also verifiable: the brief exists, covers the required fields, and can be reviewed before it generates downstream work. The required tools are relatively simple: reading, writing, search, context retrieval, and document editing. If something is not good enough, it can be revised before publication or execution.

This is a good candidate for more autonomy.

Approving a special payment condition is different. The language may be textual, but the required context is more complex. Some information is in the CRM, some is in financial data, some is in emails or messages, and some may be in the heads of the people who participated in the negotiation.

The feedback is not immediate. A decision may look correct in the moment and only show its effects weeks or months later. The impact on cash flow, margin, customer behavior, and financial predictability can take time to appear.

The task can be formally completed — approve or reject the exception — but that does not mean the decision was good. And depending on the situation, reversing the decision can be difficult or politically costly.

In this scenario, the agent can still be very useful. It can consolidate information, highlight risks, compare policies, suggest questions, and prepare a recommendation. But the final decision should probably remain with a human in the loop.

The difference between the two cases shows the central decision: productivity gains do not come from placing agents into any process. They come from choosing processes where agents can operate with enough context, tools, feedback, and control to determine whether they should have autonomy.

## Start small, test, and expand the scope

AI agents will have a major impact on knowledge work. But applying them outside software development requires more operational design than simply writing more prompts.

The safest path is to start with specific tasks, clear success criteria, available context, review mechanisms, and low cost of error. Then test the agent in a limited scope, observe where it fails, improve the context, adjust the tools, create feedback mechanisms, and only then increase its autonomy.

This logic is similar to what worked in software development, but it needs to be adapted to each area's environment.

In software, agents found fertile ground because the work already had many of the necessary elements: documented context, integrated tools, fast feedback, versioning, and objective validation.

In knowledge work, those elements need to be built.

And maybe that is the main lesson: before asking how to create agents for an area of the company, we need to ask whether that area offers the conditions for agents to work well.

When those conditions exist, the gains can be significant. When they do not, the agent's role should be more assistive, with humans maintaining judgment, responsibility, and control.

The opportunity is large. But it is not about automating entire jobs. It is about redesigning tasks, creating more agent-friendly environments, and giving agents autonomy where context, feedback, and risk allow it.
