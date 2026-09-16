ChatClaud FIX — deploy on Render

1) New Web Service → Node
2) Root = this folder (index.html + server.js + package.json)
3) Start: npm start  (or node server.js)
4) Put keys from ENV-KEYS.txt into Environment
5) Check https://YOUR.onrender.com/api/health
   expect: hasGroq:true, hasNova:true (if NOVA_* set)

Changes in this build:
- Nova search runs on almost every non-trivial question (not once)
- Sources book button under bot messages
- Thinking = white circle face + English labels (Thinking… / Searching…)
- Light theme CSS fixed
- Language switch hooks applyLanguage
- Vision: HF_KEY / HF_KEY_2 + Mistral fallback
- NOVA_AIP_TOKEN alias accepted
