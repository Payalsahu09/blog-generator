🧠 AI BlogSmith — AI-Powered Blog Generator

AI BlogSmith is a web-based AI content generator that helps users instantly create professional blog posts using OpenAI’s language models.
With an elegant UI, customizable tone, and quick generation features, it’s designed to help writers, marketers, and businesses craft quality blogs effortlessly.

✨ Features

✅ Instant Blog Generation — Create complete blog posts in seconds
✅ Customizable Tone & Length — Choose between Professional, Friendly, Casual, Academic, or Humorous tones
✅ Responsive Design — Works perfectly across desktop and mobile
✅ Interactive Animations — Built with AOS (Animate On Scroll) for smooth motion effects
✅ Modern UI — Styled using Tailwind CSS and Feather Icons
✅ Download Option — Save generated blogs for editing or publishing

🧩 Tech Stack

Frontend: HTML5, CSS3, TailwindCSS, JavaScript
Libraries:

AOS
 — Smooth scroll animations

Feather Icons
 — Clean SVG icons

TailwindCSS CDN
 — Utility-first CSS styling
Backend (optional): Can be connected to Flask / Node.js for actual OpenAI API calls

🚀 Getting Started
🔹 1. Clone the repository
git clone https://github.com/Payalsahu09/blog-generator
cd ai-blogsmith

🔹 2. Open the project

Just open the index.html file in your browser.
(If you plan to use a backend with OpenAI API, configure it as shown below.)

🔹 3. (Optional) Connect to Backend API

If you’re integrating OpenAI’s API:

Example with Flask (Python):

from flask import Flask, request, jsonify
import openai

app = Flask(__name__)
openai.api_key = "your_api_key"

@app.route('/generate', methods=['POST'])
def generate_blog():
    data = request.json
    prompt = f"Write a {data['tone']} tone blog post about {data['topic']} in {data['length']} words."
    response = openai.Completion.create(model="gpt-3.5-turbo", prompt=prompt, max_tokens=600)
    return jsonify({"blog": response.choices[0].text.strip()})


Then, connect it to your frontend using fetch() in JavaScript.

📁 Folder Structure
ai-blogsmith/
│
├── index.html        # Main frontend file
├── /static/          # Optional static assets (favicon, images, etc.)
├── /backend/         # (Optional) API server for OpenAI integration
└── README.md

💡 How It Works

The user enters a topic, selects a tone, and chooses a length.

The app shows a loading animation while generating content.

The generated content (sample or API-based) is displayed dynamically.

The user can download or copy the blog content.

🖥️ Demo Preview

Prompt: “The Future of AI in Education”
