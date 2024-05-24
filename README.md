# Gemini-explorer

# Description

An interactive Streamlit app powered by Google Gemini for engaging AI-assisted conversations. Users can input their names and queries to receive dynamic responses. The app maintains chat history and provides a seamless user experience with a fun, emoji-enhanced interface

# Task 1

### Steps to Set Up Google Cloud for Gemini Explorer Mission

1. **Create a Google Cloud Account:**

   - Go to [Google Cloud Platform](https://cloud.google.com/).
   - Sign up for a new account or log in.
   - Verify your account with billing information (no charges initially).

2. **Set Up Billing:**

   - Ensure billing information is accurate for account verification.
   - Utilize free trial credits. Upgrade to a paid account after the trial or credits end to continue using services.

3. **Create a Project for Gemini Explorer Mission:**
   - In the Google Cloud Platform dashboard, create a new project.
   - Name the project descriptively.
   - Go to the Vertex AI section and enable the recommended APIs for your project.

# Task 2

### Steps to Install and Initialize Google Cloud SDK

1. **Install Google Cloud SDK:**

   - Download the installer for your operating system from the [Google Cloud SDK webpage](https://cloud.google.com/sdk/docs/install).
   - Run the installer and follow the prompts to complete the installation.

2. **Initialize Google Cloud SDK:**
   - Open your terminal or command prompt.
   - Run `gcloud init` to start the initialization process.
   - Follow the on-screen instructions to log in to your Google Cloud account and set up your default project and configuration.

# Task 3

### Steps to Set Up Vertex AI in Your Project

1. **Import Required Libraries:**

   ```python
   import vertexai
   import streamlit as st
   from vertexai.preview import generative_models
   from vertexai.preview.generative_models import GenerativeModel, Part, Content, ChatSession
   ```

2. **Initialize Vertex AI:**

   ```python
   project = "gemini-explorer"
   vertexai.init(project=project)
   ```

3. **Load and Start the Model:**
   ```python
   config = generative_models.GenerationConfig(
       temperature=0.4
   )
   model = GenerativeModel(
       "gemini-pro",
       generation_config=config
   )
   chat = model.start_chat()
   ```
