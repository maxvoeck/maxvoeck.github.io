---
layout: page
permalink: /chatbot/
title: Chatbot
---

<style>
  .post-header, .page-heading, header.post-header {
    display: none !important;
  }

  @media (max-width: 600px) {
    .site-header {
      display: none !important;
    }
    .page-content {
      padding-top: 0 !important;
      margin-top: 0 !important;
    }
  }

  .chatbot-wrap {
    --sumi: #1a1a18;
    --kuro: #2c2c28;
    --hai: #3d3d38;
    --kinari: #f0ece4;
    --shiro: #f7f5f0;
    --kinu: #e8e3d8;
    --ishi: #b8b3a8;
    --sugi: #8a8578;
    --beni: #c45c3e;
    --matcha: #7a8c6e;
    --ai: #5b7a8c;
    --font-display: 'Cormorant Garamond', Georgia, serif;
    --font-body: 'Noto Sans', system-ui, sans-serif;
    font-family: var(--font-body);
    color: var(--sumi);
    max-width: 720px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    height: calc(100vh - 80px);
  }

  html[data-theme="dark"] .chatbot-wrap {
    --sumi: #f0ece4;
    --kuro: #e8e3d8;
    --hai: #b8b3a8;
    --kinari: #2c2c28;
    --shiro: #1a1a18;
    --kinu: #3d3d38;
    --ishi: #5a5750;
    --sugi: #8a8578;
  }

  .chat-header {
    padding: 24px 24px 16px;
    border-bottom: 1px solid var(--kinu);
  }

  .chat-header h1 {
    font-family: var(--font-display);
    font-size: 1.6rem;
    font-weight: 500;
    margin: 0 0 4px;
    color: var(--sumi);
  }

  .chat-header p {
    font-size: 0.85rem;
    color: var(--sugi);
    margin: 0;
  }

  .messages {
    flex: 1;
    overflow-y: auto;
    padding: 24px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .messages::-webkit-scrollbar { width: 5px; }
  .messages::-webkit-scrollbar-track { background: transparent; }
  .messages::-webkit-scrollbar-thumb { background: var(--ishi); border-radius: 3px; }

  .msg {
    display: flex;
    gap: 10px;
    animation: fadeIn 0.3s ease;
  }

  .msg.user { flex-direction: row-reverse; }

  .msg-avatar {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.75rem;
    flex-shrink: 0;
    font-weight: 600;
  }

  .msg.bot .msg-avatar {
    background: var(--kinu);
    color: var(--sugi);
  }

  .msg.user .msg-avatar {
    background: var(--beni);
    color: white;
  }

  .msg-bubble {
    padding: 12px 16px;
    border-radius: 16px;
    max-width: 80%;
    font-size: 0.9rem;
    line-height: 1.55;
  }

  .msg.bot .msg-bubble {
    background: var(--kinu);
    color: var(--sumi);
    border-bottom-left-radius: 4px;
  }

  .msg.user .msg-bubble {
    background: var(--beni);
    color: white;
    border-bottom-right-radius: 4px;
  }

  .msg-bubble p { margin: 0 0 8px; }
  .msg-bubble p:last-child { margin: 0; }
  .msg-bubble ul, .msg-bubble ol { margin: 4px 0; padding-left: 20px; }
  .msg-bubble li { margin: 2px 0; }
  .msg-bubble strong { font-weight: 600; }
  .msg-bubble a { color: inherit; text-decoration: underline; }

  .typing {
    display: flex;
    gap: 4px;
    padding: 12px 16px;
    align-items: center;
  }

  .typing span {
    width: 6px;
    height: 6px;
    background: var(--ishi);
    border-radius: 50%;
    animation: bounce 1.2s infinite;
  }

  .typing span:nth-child(2) { animation-delay: 0.15s; }
  .typing span:nth-child(3) { animation-delay: 0.3s; }

  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    padding: 0 24px 12px;
  }

  .chip {
    padding: 8px 16px;
    border: 1px solid var(--kinu);
    border-radius: 20px;
    background: transparent;
    color: var(--sugi);
    font-size: 0.82rem;
    cursor: pointer;
    font-family: var(--font-body);
    transition: all 0.2s;
  }

  .chip:hover {
    background: var(--kinu);
    color: var(--sumi);
  }

  .input-area {
    padding: 16px 24px 24px;
    border-top: 1px solid var(--kinu);
    display: flex;
    gap: 10px;
  }

  .input-area input {
    flex: 1;
    padding: 12px 16px;
    border: 1px solid var(--kinu);
    border-radius: 24px;
    background: var(--kinari);
    color: var(--sumi);
    font-size: 0.9rem;
    font-family: var(--font-body);
    outline: none;
    transition: border-color 0.2s;
  }

  .input-area input:focus {
    border-color: var(--beni);
  }

  .input-area input::placeholder {
    color: var(--ishi);
  }

  .input-area button {
    width: 44px;
    height: 44px;
    border: none;
    border-radius: 50%;
    background: var(--beni);
    color: white;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.2s;
  }

  .input-area button:disabled {
    opacity: 0.4;
    cursor: not-allowed;
  }

  .input-area button:hover:not(:disabled) {
    opacity: 0.85;
  }

  .error-note {
    text-align: center;
    padding: 8px;
    font-size: 0.8rem;
    color: var(--beni);
  }

  /* Mobile Responsive */
  @media (max-width: 600px) {
    .chatbot-wrap {
      height: 100vh;
      height: 100dvh;
    }

    .chat-header {
      padding: 16px 16px 12px;
    }

    .chat-header h1 {
      font-size: 1.3rem;
    }

    .chat-header p {
      font-size: 0.78rem;
    }

    .messages {
      padding: 16px 12px;
      gap: 12px;
    }

    .msg {
      gap: 8px;
    }

    .msg-avatar {
      width: 28px;
      height: 28px;
      font-size: 0.65rem;
    }

    .msg-bubble {
      max-width: 85%;
      padding: 10px 14px;
      font-size: 0.85rem;
      line-height: 1.5;
    }

    .chips {
      padding: 0 12px 10px;
      gap: 6px;
    }

    .chip {
      padding: 6px 12px;
      font-size: 0.75rem;
    }

    .input-area {
      padding: 12px 12px 16px;
      gap: 8px;
    }

    .input-area input {
      padding: 10px 14px;
      font-size: 0.85rem;
    }

    .input-area button {
      width: 40px;
      height: 40px;
      flex-shrink: 0;
    }
  }

  /* Very small screens */
  @media (max-width: 380px) {
    .msg-avatar {
      display: none;
    }

    .msg-bubble {
      max-width: 95%;
    }

    .chip {
      padding: 5px 10px;
      font-size: 0.7rem;
    }
  }

  /* Fix iOS input zoom */
  @media (max-width: 600px) {
    .input-area input {
      font-size: 16px;
    }
  }

  /* Safe area for notched phones */
  @supports (padding-bottom: env(safe-area-inset-bottom)) {
    .input-area {
      padding-bottom: calc(16px + env(safe-area-inset-bottom));
    }
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(8px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes bounce {
    0%, 60%, 100% { transform: translateY(0); }
    30% { transform: translateY(-6px); }
  }
</style>

<div class="chatbot-wrap">
  <div class="chat-header">
    <h1>Schulassistent</h1>
    <p>Studienkolleg Leipzig</p>
  </div>

  <div class="messages" id="messages">
    <div class="msg bot">
      <div class="msg-avatar">STK</div>
      <div class="msg-bubble">
        <p>Hallo! Ich bin der Schulassistent des Studienkolleg Leipzig. Wie kann ich dir helfen?</p>
      </div>
    </div>
  </div>

  <div class="chips" id="chips">
    <button class="chip" onclick="ask('Wie kann ich mich anmelden?')">Anmeldung</button>
    <button class="chip" onclick="ask('Was kostet das Studienkolleg?')">Kosten</button>
    <button class="chip" onclick="ask('Was ist die FSP?')">FSP</button>
    <button class="chip" onclick="ask('Welche Kurse gibt es?')">Kurse</button>
    <button class="chip" onclick="ask('Wann beginnt das Semester?')">Termine</button>
  </div>

  <div class="input-area">
    <input type="text" id="userInput" placeholder="Frage stellen..." autocomplete="off">
    <button id="sendBtn" onclick="send()">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
    </button>
  </div>
</div>

<script>
  const WORKER_URL = 'https://stk-chatbot.maksheinrich.workers.dev/';
  const messagesEl = document.getElementById('messages');
  const inputEl = document.getElementById('userInput');
  const sendBtn = document.getElementById('sendBtn');
  const chipsEl = document.getElementById('chips');
  let history = [];
  let sending = false;

  inputEl.addEventListener('keydown', e => {
    if (e.key === 'Enter' && !sending) send();
  });

  function ask(text) {
    inputEl.value = text;
    send();
  }

  function addMsg(role, text) {
    const div = document.createElement('div');
    div.className = `msg ${role}`;
    const avatar = role === 'bot' ? 'STK' : 'Du';
    div.innerHTML = `
      <div class="msg-avatar">${avatar}</div>
      <div class="msg-bubble">${formatText(text)}</div>
    `;
    messagesEl.appendChild(div);
    messagesEl.scrollTop = messagesEl.scrollHeight;
  }

  function formatText(text) {
    return text
      .replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>')
      .replace(/\n\n/g, '</p><p>')
      .replace(/\n- /g, '<li>')
      .replace(/\n(\d+)\. /g, '<li>')
      .replace(/\n/g, '<br>')
      .replace(/^/, '<p>')
      .replace(/$/, '</p>');
  }

  function showTyping() {
    const div = document.createElement('div');
    div.className = 'msg bot';
    div.id = 'typing';
    div.innerHTML = `
      <div class="msg-avatar">STK</div>
      <div class="typing"><span></span><span></span><span></span></div>
    `;
    messagesEl.appendChild(div);
    messagesEl.scrollTop = messagesEl.scrollHeight;
  }

  function hideTyping() {
    const el = document.getElementById('typing');
    if (el) el.remove();
  }

  async function send() {
    const text = inputEl.value.trim();
    if (!text || sending) return;

    sending = true;
    sendBtn.disabled = true;
    inputEl.value = '';

    if (chipsEl) chipsEl.style.display = 'none';

    addMsg('user', text);
    showTyping();

    history.push({ role: 'user', parts: [{ text }] });

    try {
      const res = await fetch(WORKER_URL, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ message: text, history: history.slice(-10) }),
      });

      const data = await res.json();
      hideTyping();

      const reply = data.reply || 'Entschuldigung, es gab ein Problem.';
      addMsg('bot', reply);

      history.push({ role: 'model', parts: [{ text: reply }] });
    } catch (err) {
      hideTyping();
      addMsg('bot', 'Verbindung fehlgeschlagen. Bitte versuche es erneut.');
    }

    sending = false;
    sendBtn.disabled = false;
    inputEl.focus();
  }
</script>
