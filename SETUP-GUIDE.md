# 🤖 AI Interview Platform — Setup Guide
## Zero Budget | Local | n8n + HTML

---

## 📁 Files You Got:
- `interview-frontend.html` → Open this in Chrome (your website)
- `n8n-interview-workflow.json` → Import this into n8n

---

## ⚡ Step 1: Install n8n (One Time)

```bash
# Install n8n globally
npm install -g n8n

# Start n8n
n8n start
```

Then open: **http://localhost:5678**

---

## 🔑 Step 2: Get FREE Groq API Key

1. Go to → **https://console.groq.com**
2. Sign up (free, no credit card)
3. Click "API Keys" → Create new key
4. Copy the key (starts with `gsk_...`)

---

## 📥 Step 3: Import Workflow into n8n

1. Open n8n at **http://localhost:5678**
2. Click **"New Workflow"**
3. Click the **3 dots menu** (top right) → **"Import from file"**
4. Select `n8n-interview-workflow.json`
5. Workflow loads ✅

---

## 🔗 Step 4: Add Groq Credentials in n8n

1. Click on any **"Groq"** node
2. Click "Credentials" → "Create New"
3. Name: `Groq API`
4. Paste your API key
5. Save ✅

---

## ▶️ Step 5: Activate the Workflow

1. Toggle the switch at top-right to **"Active"**
2. Your webhook is now live at:
   **http://localhost:5678/webhook/interview**

---

## 🌐 Step 6: Open the Website

1. Simply **double-click** `interview-frontend.html`
2. OR open Chrome and drag the file in
3. Allow Camera + Microphone when asked
4. That's it! 🎉

---

## 🧪 How it Works:

```
You fill profile form
        ↓
HTML sends to n8n webhook
        ↓
n8n calls Groq AI (LLaMA 3.3 70B - FREE)
        ↓
AI generates interview question
        ↓
You answer (voice or text)
        ↓
AI scores your answer + asks next question
        ↓
After 5 questions → Full report with score!
```

---

## 💡 Demo Mode (No n8n):

The HTML file works **WITHOUT n8n** too!
- It uses built-in fallback questions
- Still does webcam + voice + scoring (simulated)
- Perfect for quick demos

---

## 🚀 Future Upgrades (Still Free):

| Feature | Tool | Cost |
|---------|------|------|
| Real emotion detection | MediaPipe (Google) | Free |
| Better AI model | Gemini Flash API | Free tier |
| Save interview history | Supabase free tier | Free |
| Deploy online | Render / Railway | Free |

---

## ❓ Troubleshooting:

**n8n not connecting?**
→ HTML works in demo mode automatically. No worries!

**Camera not working?**
→ Must open in Chrome. Allow camera permission.

**Voice not working?**
→ Chrome only. Click mic button once.

**Groq API error?**
→ Check API key in n8n credentials. Make sure workflow is Active.
