# Crew-AI-Crash-course
# Youtube Videos to Blog Page Using CrewAI Agents

This project uses **CrewAI Agents** to transform YouTube video content into a comprehensive blog post. It involves a sequence of tasks: research and writing. The project integrates CrewAI's task-oriented agents to interact with a YouTube channel, gather video content, and generate a well-structured blog post.

---

## Project Structure

1. **agent.py**  
   This file defines the two agents responsible for research and writing. The **Blog Researcher** agent fetches video content from YouTube, and the **Blog Writer** agent creates a blog post based on the video information.

2. **crew.py**  
   This file configures and manages the **Crew** of agents and tasks, including sequential execution of the research and writing tasks, memory management, and feedback.

3. **task.py**  
   This file defines the **research** and **writing** tasks, including the description, expected output, and the tools each task utilizes (like the YouTube Channel Search Tool).

4. **tool.py**  
   Contains the `YoutubeChannelSearchTool` for searching and retrieving videos from a specific YouTube channel.

---

## Features

- **Automated YouTube Research:**  
   The **Blog Researcher** agent fetches video information from the provided YouTube channel on a given topic.

- **Content Generation:**  
   The **Blog Writer** agent creates a well-structured, three-paragraph blog post summarizing the video content.

- **Task Management:**  
   Tasks are executed sequentially, ensuring that the research and writing steps are completed in an orderly fashion.

- **Customizable Topic Handling:**  
   Users can provide a topic, and the agents will retrieve relevant videos and generate blog content accordingly.

- **AI-Powered with OpenAI GPT-4:**  
   The agents leverage the **OpenAI GPT-4** model to process and generate the final blog content.

---

## Installation and Setup

### Prerequisites

1. **Python 3.7 or higher**  
   Ensure Python 3.7 or higher is installed.

2. **Anaconda or Miniconda Installed:**  
   Install Miniconda or Anaconda if you don’t already have it. You can download it from [here](https://www.anaconda.com/products/individual).

3. **Environment Variables:**  
   Ensure you have your **OpenAI API Key** available for this project.

### Setting Up the Environment

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   
2. **Create a Conda Environment:**
   bash
   conda create -n yt-blog-crew python=3.8 -y
   
3.**Activate the Environment:**
   bash

  conda activate yt-blog-crew
  
4.**Install Dependencies:**
  Install the required libraries using requirements.txt:
   bash 
   pip install -r requirements.txt
   
5.**Set Up Environment Variables:**
Create a .env file in the project root with the following content:
  bash
  OPENAI_API_KEY=your_openai_api_key
  GROQ_API_KEY=your_groq_api_key
  
1.**How to Run**
  Run the Crew Task Execution:
  Start the task execution by running the following Python script:
   bash
   python crew.py
   
2.**Interact with the System:**

**Provide a Topic:**
  - The system requires a topic to start the research and writing process (e.g., "AI vs ML vs DL vs Data Science").

**Task Execution:**
  - The research_task retrieves relevant video information from the provided YouTube channel, and the write_task generates a blog post.

**View Output:**
 - The final blog post will be saved in a file, for example, new-blog-post.md.

**Code Overview**
 - Agent Configuration:
   Agents like blog_researcher and blog_writer are configured with specific goals to handle the research and writing tasks, respectively.

 - Task Definitions:
   The research and writing tasks define the descriptions, expected outputs, and tools required for each task. The YoutubeChannelSearchTool is used for searching YouTube videos.

 - Crew Management:
   The Crew class orchestrates the agents and tasks, with an option to manage task execution sequentially.
