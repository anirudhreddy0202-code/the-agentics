# CrewAI Build Report

**Name:** Anirudh Reddy Bommineni

**Topic I used:** Holiday shopping trends

## 1. What I changed

I modified the Technical Writer agent in `main.py`. Originally, its goal was to explain the topic to a general reader, and its backstory focused on making technical material clear and jargon-free. I changed the goal to target business executives and emphasize business impact, practical implications, and strategic decisions. I also changed the backstory to describe an executive communications specialist who prepares concise briefings for business leaders. I chose this change because I wanted the final report to be more useful for people making business decisions. I did not change the holiday shopping topic between the two runs, allowing me to compare how the different instructions influenced the output.

## 2. How CrewAI works

CrewAI organizes an AI workflow around agents, tasks, and a crew. An agent has a role, a goal, and a backstory that guide how it approaches its work. In this project, the workflow uses agents for research, writing, and editing. Tasks describe the work that needs to be completed, while the crew coordinates the agents to carry out the workflow.

The Technical Writer's instructions influence how it presents information. In my original run, the report mainly summarized holiday shopping trends for a general audience. After I changed the writer's goal and backstory, the second report emphasized business implications and recommendations for retailers. For example, it included suggestions about mobile checkout, early-season marketing, sustainability messaging, buy-now-pay-later options, and inventory management.

This experiment showed me that an agent's instructions can influence the focus, structure, and style of its output. However, changing the instructions does not guarantee that the information will be accurate. The generated claims still need to be checked independently.

## 3. Evidence

The original output, `explainer_run1.md`, summarized five holiday shopping trends, including e-commerce growth, earlier purchasing, experience-focused gifts, sustainability, and omnichannel retail.

The modified output, `explainer_run2.md`, focused more on business implications and actionable recommendations. It discussed mobile-first checkout, early-season marketing, sustainability messaging, buy-now-pay-later options, and dynamic inventory management.

The comparison shows that changing the Technical Writer's goal and backstory influenced the report's emphasis and intended audience.

One limitation was that the generated reports included statistics marked `[source needed]`. I kept this limitation in mind because the workflow did not independently verify those claims.

## 4. Choosing a framework

I chose CrewAI because its agent-based structure made it straightforward to understand how different roles contribute to a workflow. The project separates research, writing, and editing responsibilities, making it easier to experiment with an individual agent's instructions and compare the resulting reports.

Another framework from the assignment is LangGraph. LangGraph would be useful for workflows that need more explicit control over how steps connect, including conditional paths, repeated steps, and state management. However, that additional control could require more configuration than this relatively simple workflow needs.

For this experiment, CrewAI was a suitable choice because my main goal was to change an agent's instructions and observe the effect on the final output. I based this choice on the structure of the starter kit and the behavior I observed in the two runs, rather than on a benchmark comparing the frameworks.

## 5. Verification and AI use

I verified that the CrewAI setup worked by running `uv run python check_setup.py` and confirming that it displayed `CrewAI kit OK`. I also ran the workflow twice using the same topic and compared `explainer_run1.md` with `explainer_run2.md` to check whether the output changed after modifying the Technical Writer agent.

The generated reports contained statistics marked `[source needed]`. I did not independently verify those statistics, so they should not be treated as confirmed facts. The workflow's output is useful for demonstrating the effect of agent instructions, but factual claims require separate verification.

I used ChatGPT for setup troubleshooting, step-by-step coding guidance, and help organizing this report. I reviewed the code changes and compared the generated outputs to describe the observed differences. I understand that AI assistance can make mistakes, so I have distinguished the output comparison from claims that still need independent fact-checking.