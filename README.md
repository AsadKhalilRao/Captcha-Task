# 🤖 Can AI Beat You? — The CAPTCHA Challenge

An interactive, web-based educational game designed for classroom AI literacy (ages 5–12). Inspired by real research from the **Open CaptchaWorld** study (Luo et al., 2025), this app lets students play visual and logical puzzle challenges against advanced AI models using the Groq Vision API. 

The project demonstrates why human brains excel at visual recognition, common sense, and spatial sequencing—areas where AI models often struggle.

---

## 🌟 Key Features

* **Real AI Integration:** Play live against AI vision models (via the Groq Vision API using `qwen/qwen3.6-27b`).
* **6 Gamified Challenge Types:**
  1. 🎲 **Dice Dot Counter:** Count overlapping dice dots (AI real-world accuracy: 0%).
  2. 🔤 **Warped Word Reader:** Read distorted, noisy text CAPTCHAs.
  3. 🔢 **Click-in-Order Challenge:** Locate and sequence numbers 1 through 6 sequentially.
  4. 😵 **Don't Be Fooled!:** Tricky, misleading logic and instruction puzzles.
  5. 🐾 **Animal Grid Hunt:** Spot all target animal tiles in a 3×3 grid without selecting false positives.
  6. 🧩 **Pattern Fixer:** Predict the next shape and color combination in a repeating sequence.
* **Live Scoreboard & Leaderboard:** Real-time round and score tracking alongside research data comparing human accuracy (93.3%) to various AI models (OpenAI o3, GPT-4.1, Gemini 2.5 Pro, Claude 3.7, etc.).
* **In-Browser Canvas Rendering:** Puzzles generate dynamically on HTML5 Canvas elements.
* **Zero Dependencies:** Fully self-contained inside a single HTML file—no framework build steps or external JavaScript libraries needed.

---

## 🛠️ Prerequisites & Setup

### Requirements
* Any modern web browser (Chrome, Edge, Firefox, Safari).
* An active internet connection (for loading Google Fonts and making Groq API requests).
* *(Optional)* A **Groq API Key** to enable live AI responses.

### Running the App
1. Open `CAPTCHA_Challenge_fixed (1).html` directly in your browser.
2. Click the **"Add Key"** button in the header bar to enter a Groq API key.
   * *Note:* The API key is stored securely in temporary memory only for the current browser session.
3. Select any game tab to start playing against the computer!

---

## 📂 Code Structure

The file is structured as a single-page web application:

| Section | Description |
| :--- | :--- |
| **CSS Styles (`<style>`)** | Bright, kid-friendly design variables, responsive grid layouts, animations, and UI states. |
| **Scoreboard & Leaderboard** | Displays live human vs. AI points and benchmark performance graphs from academic research. |
| **Activity Cards (`.activity-panel`)** | HTML markup for each of the 6 game modules with canvas displays and interactive inputs. |
| **State & API Handling (`<script>`)** | Tracks current game states, generates random canvas images, handles human interaction, and dispatches base64 image prompts to the Groq API (`askGroqVision`). |

---

## 🔬 Research Background

This application is modeled after research published in **Open CaptchaWorld** (Luo et al., 2025), which evaluated AI performance across 225 puzzles and 20 puzzle categories. The benchmark highlighted significant gaps in current AI vision and spatial reasoning capabilities:

* **Humans:** ~93.3% overall accuracy
* **OpenAI o3:** ~40.0%
* **GPT-4.1 / Gemini 2.5 Pro:** ~25.0%
* **Claude 3.7:** ~20.0%
* **GPT-4o:** ~5.7%
