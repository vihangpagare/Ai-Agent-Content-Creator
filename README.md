# Ai-Agent-Content-Creator
An AI-powered LinkedIn content creation agent that generates high-quality, personalized posts by researching trending topics, analyzing competitor content, and integrating article insights.

Features
Smart Topic Generation: AI-generated content topics based on your profile and industry

Article Research: Fetches and evaluates relevant articles for content inspiration

Competitor Analysis: Analyzes high-performing LinkedIn posts in your niche

Content Optimization: Creates LinkedIn-optimized posts with engagement triggers

Direct LinkedIn Posting: Automatically posts content to your LinkedIn profile

Memory System: Maintains context about your profile and preferences

Project Structure
text
linkedin-content-agent/
│
├── .env                # Environment variables (credentials)     
├── README.md           # This file
│
├── prompts.py          # All AI prompt templates
├── agent_nodes.py      # Individual workflow functions
├── agent.py            # Main graph assembly and state
├── streamlit_ui.py     # Web interface
│
└── requirements.txt    # Python dependencies
Setup Instructions
1. Clone the Repository
bash
git clone <repository-url>
cd linkedin-content-agent
2. Install Dependencies
bash
pip install -r requirements.txt
3. Configure Environment Variables
Create a .env file in the root directory:



text
# Azure OpenAI Configuration
AZURE_OPENAI_API_KEY=your_azure_openai_api_key_here
AZURE_OPENAI_ENDPOINT=https://your-endpoint.openai.azure.com/
AZURE_OPENAI_API_VERSION=2024-05-01-preview
AZURE_OPENAI_MODEL=gpt4o

# EXA Search API
EXA_KEY=your_exa_api_key_here

# LinkedIn API Configuration
LINKEDIN_ACCESS_TOKEN=your_linkedin_access_token_here
LINKEDIN_PERSON_URN=urn:li:person:your_person_id_here
4. API Setup Guide
Azure OpenAI
Create an Azure OpenAI resource in Azure Portal

Deploy a GPT-4 model

Copy the API key, endpoint, and version

EXA Search API
Sign up at EXA

Get your API key from the dashboard

LinkedIn API
Create a LinkedIn Developer Application

Obtain access token with necessary permissions

Get your Person URN from LinkedIn API

Usage
1. Start the Application
bash
streamlit run streamlit_ui.py
2. Initial Setup
Enter User ID: Provide a unique identifier for your session

Update Profile: Paste your complete LinkedIn profile information

Generate Content: Click "Generate Topics & Create Content"

3. Content Workflow
The agent follows this workflow:

Profile Analysis: Understands your background and expertise

Topic Generation: Creates relevant content topics

Topic Selection: Automatically selects the best topic

Article Research: Finds and evaluates relevant articles

Competitor Analysis: Analyzes high-performing posts

Content Creation: Generates draft content

Content Optimization: Refines for maximum engagement

Review & Post: Option to approve and post to LinkedIn

4. Dashboard Features
Workflow Status: Real-time updates on content generation

Analytics: Progress tracking and quality metrics

Profile Management: View and manage stored profile data

Content Review: Preview generated content
