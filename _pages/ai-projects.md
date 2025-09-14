---
permalink: /ai-projects/
title: "AI & Data Science Projects"
excerpt: "AI & Data Science Projects"
author_profile: true
redirect_from: 
  # - /about/
  # - /about.html

#Example: editing a markdown file for a talk
#![Editing a markdown file for a talk](/images/editing-talk.png)
---
*I am currently curating this list. Please find my GitHub and GitLab projects at:*    
<a href="https://github.com/siliconshells/GITLAB_Projects" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: semi-bold; font-size: 15px;">
  GitLab Projects →
</a>            
<a href="https://github.com/siliconshells" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: semi-bold; font-size: 15px;">
  GitHub Projects →
</a>


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px; background-color: #f4f9ffff;">
  
  <div style="flex: 1; ">
    <h3 style="margin: 0 0 12px 0;">A RAG Application using LangGraph</h3>
  </div>

  <div style="display: flex;">
    <!-- Left Column (Title + Image + GitHub Link) -->
    <div style="flex: 0 0 200px; margin-right: 20px;">
      <img src="/images/main_app.png" alt="Project Thumbnail" style="width: 100%; height: auto; border-radius: 6px; border: 1px solid #ddd;" />
    </div>
    <!-- Right Column (Description) -->
    <div style="flex: 1; display: flex;">
      <p style="margin: 0; padding: 4px 0;font-size: 15px;">
        This project demonstrates a <strong>LangGraph</strong> pipeline served with <strong>FastAPI + Strawberry GraphQL</strong>, integrated with vector search in <strong>Pinecone</strong>. A crawler scans my website to collect all accessible links, and the contents are loaded and chunked for efficient processing by the models. Embeddings are then generated from these chunks and stored in Pinecone for later retrieval.    
        <br>
        When a user enters a question in the <strong>Flask</strong> frontend, it is sent to the <strong>FastAPI GraphQL</strong> backend, which triggers the execution of the <strong>LangGraph</strong> pipeline. An embedding is created from the question, and a similarity search is performed in Pinecone to find semantically related text. This context is combined with the question to form a prompt for <strong>Google's Gemini Flash</strong> chat model. The answer is returned through the same pipeline and displayed to the user.   
        <br>
        The RAG application is designed to be adaptable: it can work with any website by changing the target domain in the GitHub code, and it can be extended to other data sources by modifying the loader.    
      </p>  
    </div>
  </div>
  <div style="flex: 1; ">
    <div style="display: flex; align-items: center; justify-content: space-between; margin-top: 3px;font-size: 13px;">
      <a href="https://langgraph-rag.leonardeshun.com" target="_blank" style="color: #0955abff; text-decoration: none; font-weight: bold;">
        Live Demonstration →
      </a>
      <a href="https://github.com/siliconshells/langchain_RAG" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: bold;">
        View on GitHub →
      </a>
    </div>  
  </div>
</div>


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px; background-color: #f4f9ffff;">
  
  <div style="flex: 1; ">
    <h3 style="margin: 0 0 12px 0;">Integration of LLM into an application</h3>
  </div>

  <div style="display: flex;">
    <!-- Left Column (Title + Image + GitHub Link) -->
    <div style="flex: 0 0 200px; margin-right: 20px;">
      <img src="/images/tmb_streamlit_on_aws.png" alt="Project Thumbnail" style="width: 100%; height: auto; border-radius: 6px; border: 1px solid #ddd;" />
    </div>
    <!-- Right Column (Description) -->
    <div style="flex: 1; display: flex;">
      <p style="margin: 0; padding: 4px 0;font-size: 15px;">
        I used Python and  Streamlit to create a web application that connects to <strong>OpenAI's GPT2</strong>, hosted on Hugging Face to complete a sentence. It then uses <strong>SD-Turbo</strong> to generate a related image and <strong>Toxic-BERT</strong> to check for inappropriate content generation by the LLM. GitHub CI/CD was used to push the code to an <strong>AWS EC2 instance</strong> hosting the application.
      </p>
    </div>
  </div>
  <div style="flex: 1; ">
    <div style="text-align: right; margin-top: 3px;font-size: 13px;">
      <a href="https://gitlab.com/dukeaiml/ids721-spring2025/Leonard_Eshun_Mini_Project_Eight" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: bold;">
        View on GitLab →
      </a>
    </div>  
  </div>
</div>


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px; background-color: #f4f9ffff;">
  
  <div style="flex: 1; ">
    <h3 style="margin: 0 0 12px 0;">Text Search with Vector Databases</h3>
  </div>

  <div style="display: flex;">
    <!-- Left Column (Title + Image + GitHub Link) -->
    <div style="flex: 0 0 200px; margin-right: 20px;">
      <img src="/images/tmb_qdrantg.png" alt="Project Thumbnail" style="width: 100%; height: auto; border-radius: 6px; border: 1px solid #ddd;" />
    </div>
    <!-- Right Column (Description) -->
    <div style="flex: 1; display: flex;">
      <p style="margin: 0; padding: 4px 0;font-size: 15px;">
        Written in Rust and containerized with <strong>Docker</strong> using the Amazon Linux 2023 base image during the <strong>CI/CD</strong> process in GitLab. The image was pushed to <strong>Amazon Elastic Container Registry</strong> and used to create a <strong>Lambda function with an API gateway</strong> to serve the search function. Its main function is to connect to a <strong>Qdrant vector database</strong> and do a vector search using the text provided to the API. It returns records containing semantically similar words. 
        <br>
        The vector database was populated with information on movies from a <strong>JSONL</strong> file, and the embeddings were created with Cohere’s Embed API.
      </p>
    </div>
  </div>
  <div style="flex: 1; ">
    <div style="text-align: right; margin-top: 3px;font-size: 13px;">
    <a href="https://gitlab.com/dukeaiml/ids721-spring2025/leonard_eshun_mini_project_five" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: bold;">
      View on GitLab →
    </a>
  </div>  
  </div>
</div>
