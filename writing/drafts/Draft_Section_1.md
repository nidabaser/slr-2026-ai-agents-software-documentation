> _This is a draft version for Section 1: Introduction - 10.04.2026_

### SECTION 1 : INTRODUCTION

#### Context and Motivation

For software developers, understanding the program they will be working on takes up approximately 58% of their time (Xia et al., 2018). The greatest resource they can utilize during this process is the software's documentation. If this documentation is high-quality, it not only increases developer productivity but also facilitates the recruitment of new employees. Software with high-quality documentation prevents the accumulation of technical debt and is also efficient in terms of reusability. For example, even if the original developers who wrote the code cannot be reached, the risks in terms of maintenance and sustainability are definitely lower compared to software with low-quality documentation (De Souza, 2005; Etemadi, 2022). However, even in the most widely used open-source repositories on the popular version control system GitHub platform, the docstring coverage rate consistently falls below 30% (Yang et al., 2025). The existing documentation is often incomplete, contradicts the basic code structure, or is completely absent in components that are frequently modified (Aghajani et al., 2019).

It is known that studies on automated documentation generation have been ongoing since the 2000s to solve this problem. For example, after methods such as template-based methods, information retrieval, and deep learning-based summarizers, approaches supported by the Big Language Model have been developed (Forward, 2002). With each method and tool, it is observed that documentation is gradually approaching human quality. Some popular open and closed-source models such as GPT-4 (OpenAI, 2023), CodeLlama (Rozière et al., 2023), and DeepSeek Coder (Guo et al., 2024) have been shown to be of the same or higher quality as documentation written by developers (Yang et al. 2025; Etemadi and Robles, 2025).

While these developments seem like promising solutions to the documentation debt problem, a more detailed look is necessary because there is currently a shift from LLM-based code summarizers to AI agents. Of course, AI agents are expected to be involved not only in the documentation generation phase but also in phases such as rewriting existing documentation according to code changes in the project.

#### AI Agents for Software Documentation

An agent is a system that understands its environment and takes actions to achieve its goal (Russell & Norvig, 2020). In this study, we define an AI agent customized for software documentation as a system with the following characteristics:
1. Able to use at least one major language model for reasoning,
2. Having the goal of generating/updating software documentation,
3. Having the ability to process not only with a single inference call but also with persistent memory, tools, and multiple steps.

Thanks to the above definition, we are deliberately excluding only simple, request-based LLM inference systems so that we can include approaches involving IDE plugins with memory, automated pipelines with Git integration, and the use of multiple agents.
Because the problem of generating documentation has already been largely solved, we can say that systems where it is unclear when, how, and by whom the generated documentation will be updated as code development continues do not provide a complete solution to the documentation debt problem.

> _This is a draft version for Section 1: Introduction - 10.04.2026_