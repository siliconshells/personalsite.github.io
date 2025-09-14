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
<br >
<a href="https://github.com/siliconshells" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: semi-bold; font-size: 15px;">
  GitHub Projects →
</a>


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px;">
  
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
        This project shows a <strong>LangGraph</strong> pipeline served with <strong>FastAPI + Strawberry GraphQL</strong> with vector search in <strong>Pinecone</strong>. A crawler crawls my website to get all loadable links. The contents are loaded and chunked for easier processing by the models. Embeddings are created from the chunks and stored in Pinecone for later retrieval.    
        A question is entered into the <strong>Flask</strong> frontend application. It's sent to the <strong>FastAPI GraphQL</strong> backend which calls the function to start executing the steps of the <strong>LangGraph</strong>. An embedding is created from the question and a similarity search done in Pinecone to find semantically related text to the question.    
        This is the context, and it is added to the question to create a prompt for <strong>Google's Gemini Flash</strong> chat model. The answer is returned through the same pipeline and displayed to the user.    
        This RAG application can be used for any website by changing the website in the code on GitHub. It can also be adapted for other data sources by changing the loader.
      </p>  
    </div>
  </div>
  <div style="flex: 1; ">
    <div style="text-align: right; margin-top: 3px;font-size: 13px;">
      <a href="https://github.com/siliconshells/langchain_RAG" target="_blank" style="color: #0366d6; text-decoration: none; font-weight: bold;">
        View on GitHub →
      </a>
    </div>  
  </div>
</div>


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px;">
  
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


<div style="display: flex; flex-direction: column; border: 1px solid #6c85b4ff; border-radius: 8px; padding: 16px; margin: 16px 0; max-width: 750px; ">
  
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
        Written in Rust and containerized with <strong>Docker</strong> using the Amazon Linux 2023 base image during the <strong>CI/CD</strong> process in GitLab. The image was pushed to <strong>Amazon Elastic Container Registry</strong> and used to create a <strong>Lambda function with an API gateway</strong> to serve the search function. Its main function is to connect to a <strong>Qdrant vector database</strong> and do a vector search using the text provided to the API. It returns records containing semantically similar words. The vector database was populated with information on movies from a <strong>JSONL</strong> file, and the embeddings were created with Cohere’s Embed API.
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
