# ai-intern-assignment-kshitij-vats

Student Lead Capture & Automation System

Author: Kshitij Vats

Email: kshitijvats1023@gmail.com

Date of Submission: June 5, 2026

Project Overview
This project implements a full-stack automation system that captures student leads through a web interface and processes them using n8n workflows.

Part A: Form Design
Contains the initial frontend structure.

How to run: Open part-a/index.html in any web browser. It features client-side validation to ensure all mandatory fields are filled before submission.

Part B: n8n Workflow Configurations
Contains the backend automation logic.

Workflow B1 (Lead Capture): Captures data via Webhook, cleans it using a Set node, and routes it based on course level using an IF node.

Workflow B2 (Scheduled Fetch): Uses the JSONPlaceholder API.

Why: I chose this API because it is a reliable, free, and public testing service that provides realistic JSON structures, making it perfect for demonstrating scheduled data fetching without requiring authentication keys.

How to test: Import the .json files into your n8n instance and click "Execute Workflow."

Part C: Integration
Connects the frontend to the backend.

How to run: Update the fetch() URL in part-c/index.html with your specific n8n webhook endpoint and submit the form.

Live Demo: https://drive.google.com/file/d/16yC0PIS61RxKDKKiW53HlKDEAAQ6J-HP/view?usp=sharing

Configuration & Credentials
n8n Webhook URL: Replace [YOUR_N8N_URL] in the script with your local instance URL (e.g., your local host link and path link of test url)

Environment Variables: This project uses no sensitive API keys; however, for production, n8n credentials should be managed via the n8n "Credentials" tab, and sensitive URLs should be stored in your server's .env file.

Challenges Faced
The main challenge was establishing the connection between the browser's fetch request and the local n8n instance. I resolved this by ensuring the n8n webhook was set to "Test" mode and correctly mapping the JSON headers in the JavaScript fetch call to match the expected input format of the Webhook node.

