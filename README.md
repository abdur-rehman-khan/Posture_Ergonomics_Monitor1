#  PostureCoach — Real-Time Posture Analysis

**Real-time posture monitoring and AI-powered ergonomic coaching in your browser.**

PostureCoach uses MediaPipe Pose to analyze body landmarks, classify posture, and provide instant feedback. Its optional AI Coach offers personalized ergonomic suggestions using the Hugging Face Inference API.

## ✨ Features

- 📷 **Real-time camera analysis** — Detects 33 body landmarks using MediaPipe Pose and analyzes shoulder, neck, and torso angles.
- ✅ **Posture classification** — Identifies good posture and slouching with color-coded visual feedback and a skeleton overlay.
- 📊 **Live dashboard** — Tracks good and bad frames, session duration, alert streaks, and posture-angle trends.
- 🔔 **Smart alerts** — Configurable sound alarms and browser notifications when poor posture is detected.
- 🤖 **AI Coach** — Supports multiple LLM options through the Hugging Face Inference API, including Llama, Mistral, Phi, Gemma, and Qwen families.

## 🚀 Getting Started

### Prerequisites

- A modern web browser.
- A webcam.
- An internet connection to load MediaPipe assets and use AI features.
- A Hugging Face access token if you want to use the AI Coach.

### Option 1: Clone the repository

Clone the project from GitHub:

```bash
git clone https://github.com/abdur-rehman-khan/Posture_Ergonomics_Monitor1.git
cd Posture_Ergonomics_Monitor1
```

Open the project in VS Code or your preferred editor.

If the project contains an `index.html` file in its root directory, you can serve it locally with Python:

```bash
python -m http.server 8000
```

Then visit:

http://localhost:8000

Using `localhost` helps ensure that browser camera permissions work correctly.

### Option 2: Download the ZIP

1. Visit the [PostureCoach GitHub repository](https://github.com/abdur-rehman-khan/Posture_Ergonomics_Monitor1).
2. Click **Code → Download ZIP**.
3. Extract the files.
4. Open the project using a local development server.

## 🖥️ How to Use

1. Open PostureCoach in your browser.
2. Click **Start Camera** and grant camera permission.
3. Position yourself in the camera frame.
4. Allow the app to analyze your posture and display feedback.
5. Review your dashboard for posture statistics and trends.
6. Open the **AI Coach** tab if you want additional ergonomic suggestions.
7. Enter your Hugging Face token, select an available model, and submit your question.

## 🤖 AI Models

The application is designed to support models from the following families through the Hugging Face Inference API.

| Provider | Model families |
|---|---|
| Meta | Llama 3.2 3B, Llama 3.1 8B |
| Mistral | Mistral 7B, Mixtral 8x7B |
| Microsoft | Phi-3 Mini, Phi-3.5 Mini |
| Google | Gemma 2 2B, Gemma 2 9B |
| Qwen | Qwen2.5 3B, Qwen2.5 7B |

Model availability, provider support, access requirements, and API limits may change. Actual availability depends on the model IDs configured in the application and the Hugging Face Inference API.

### Setting up the Hugging Face token

1. Sign in to [Hugging Face](https://huggingface.co/).
2. Create an access token in [Token Settings](https://huggingface.co/settings/tokens).
3. Grant only the permissions required for your use case.
4. Enter the token in the AI Coach interface.

**Security:** Never commit your access token to GitHub. A token entered in a browser application is not a secure server-side secret; use a backend proxy if you need to protect shared credentials in a production deployment.

## 🌐 Deployment

PostureCoach can be deployed as a static web application if all required functionality is implemented in browser-side code.

Potential hosting options include:

- [GitHub Pages](https://pages.github.com/)
- [Cloudflare Pages](https://pages.cloudflare.com/)
- [Netlify](https://www.netlify.com/)
- [Vercel](https://vercel.com/)

### Deploy with GitHub Pages

1. Open the [repository](https://github.com/abdur-rehman-khan/Posture_Ergonomics_Monitor1).
2. Navigate to **Settings → Pages**.
3. Select **Deploy from a branch**.
4. Choose the `main` branch and the root (`/`) directory, if your `index.html` is located there.
5. Save and wait for the deployment to finish.

Your expected site URL will be:

`https://abdur-rehman-khan.github.io/Posture_Ergonomics_Monitor1/`

This URL will work once GitHub Pages is enabled and deployment succeeds.

**Deployment note:** GitHub Pages cannot run backend code or securely store API secrets. If the project requires a backend or a secure AI proxy, deploy that component separately.

## 🔒 Privacy

- **Camera video:** Posture analysis is designed to run locally in your browser.
- **Pose landmarks:** Processed locally by MediaPipe when the application is configured for browser-side inference.
- **AI requests:** Questions or other content sent to the AI Coach are transmitted to the selected Hugging Face service.
- **Access tokens:** Avoid storing or exposing tokens in source code, public repositories, or client-side configuration files.

Review the application code and the privacy policies of any external services you use before processing sensitive information.

## ⚠️ Medical Disclaimer

PostureCoach provides general posture feedback and AI-generated ergonomic suggestions for educational and wellness purposes. It is not a medical diagnostic tool and does not replace advice from a qualified healthcare professional.

## 📄 License

This project is intended to use the MIT License. See the `LICENSE` file in the repository for the full license text.

---

Developed by [Abdur Rehman Khan](https://github.com/abdur-rehman-khan).

If you find PostureCoach useful, consider giving the repository a ⭐ on GitHub.
