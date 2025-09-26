# CrewAI Multi-Agent System for Content Creation

This project demonstrates a multi-agent system for researching and writing articles using the [crewAI](https://github.com/crewAIInc/crewAI) framework. It showcases how multiple AI agents can collaborate on a complex task, such as content creation.

## Overview

The system is composed of a "crew" of AI agents that work together to research a given topic, write an article, and edit it to meet quality standards. This project is based on the `L2_research_write_article.ipynb` notebook.

The workflow is as follows:
1.  A **Planner** agent creates a detailed content plan.
2.  A **Writer** agent uses the plan to write an article.
3.  An **Editor** agent reviews and refines the article.

This entire process is orchestrated by a `Crew` that manages the agents and their tasks.

## Agents

The following agents are defined:

-   **Content Planner**: Responsible for planning engaging and factually accurate content on a given topic. It analyzes trends, identifies the target audience, and creates a content outline.
-   **Content Writer**: Writes an insightful and factually accurate opinion piece based on the plan provided by the Content Planner.
-   **Editor**: Edits the blog post to align with the organization's writing style, ensuring it follows journalistic best practices and maintains a balanced viewpoint.

## Tasks

The agents perform the following tasks in sequence:

1.  **Plan**: The Planner agent creates a comprehensive content plan, including an outline, audience analysis, SEO keywords, and relevant sources.
2.  **Write**: The Writer agent crafts a compelling blog post based on the content plan, incorporating SEO keywords and ensuring a clear structure.
3.  **Edit**: The Editor agent proofreads the blog post for grammatical errors and ensures it aligns with the brand's voice.

## Getting Started

### Prerequisites

This project uses `uv` for package management. The dependencies are listed in the `pyproject.toml` file.

- Python >= 3.10
- `uv`

### Installation

1.  Clone the repository:
    ```sh
    git clone https://github.com/tgohblio/crewai_multiagent.git
    cd crewai_multiagent
    ```

2.  Install the dependencies using `uv`:
    ```sh
    uv sync
    ```

3.  Create a `.env` file in the root of the project and add your API keys. For example, for OpenRouter:
    ```
    OPENROUTER_API_KEY="your_openrouter_api_key"
    ```

### Running the Project

The main logic is in the `L2_research_write_article.ipynb` Jupyter Notebook. You can run the cells in the notebook to see the agents in action.

1.  Start a Jupyter server.
2.  Open `L2_research_write_article.ipynb`.
3.  Run the cells sequentially.

You can change the topic in the following cell to have the crew write about a different subject:
```python
result = crew.kickoff(inputs={"topic": "Your New Topic Here"})
```
