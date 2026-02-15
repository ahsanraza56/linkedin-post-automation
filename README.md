# 🚀 AI-Powered LinkedIn Post Automation

A fully automated workflow built on **n8n** that takes a simple topic, generates engaging content using **Google Gemini**, creates a relevant image using **Hugging Face**, and publishes directly to **LinkedIn**.

##  workflow Overview

![Workflow Diagram](image.png) **

This tool automates the entire content supply chain:
1.  **Input:** Accepts a post topic (Manual trigger or Form).
2.  **AI Writing:** Uses **Google Gemini** to draft a professional LinkedIn post.
3.  **Structuring:** Parses the AI output to separate the post body from image prompts.
4.  **AI Visuals:** Sends the prompt to **Hugging Face** to generate a custom image.
5.  **Publishing:** Uploads the text and image to **LinkedIn** automatically.

## 🛠️ Tech Stack

* **Workflow Engine:** [n8n](https://n8n.io/)
* **LLM (Text):** Google Gemini Chat Model
* **Image Generation:** Hugging Face Inference API
* **Destination:** LinkedIn API

## ⚙️ Setup & Configuration

### Prerequisites
* An n8n instance (Self-hosted or Cloud).
* **Google Gemini API Key** (via Google AI Studio).
* **Hugging Face Access Token** (Read permission).
* **LinkedIn Developer App** (Client ID & Secret with `w_member_social` scope).

### Installation
1.  Clone this repository:
    ```bash
    git clone [https://github.com/your-username/linkedin-post-automation.git](https://github.com/your-username/linkedin-post-automation.git)
    ```
2.  Open your n8n dashboard.
3.  Click **"Import Workflow"** and select the `.json` file from this repository.
4.  Configure your credentials in the n8n credential manager for:
    * `Google Gemini API`
    * `Hugging Face API`
    * `LinkedIn OAuth2`

## 🧩 How to Use

1.  **Activate the Workflow:** Ensure the workflow is set to 'Active' in n8n.
2.  **Trigger:** Run the "Collect Post Topic" node (or use the webform URL if configured).
3.  **Input:** Enter your desired topic (e.g., *"The future of AI in web development"*).
4.  **Result:** The workflow will generate the text, create an image, and publish the post to your profile immediately.

## 🤝 Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any enhancements or bug fixes.

## 📄 License

This project is licensed under the MIT License.
