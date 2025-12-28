---
layout: default
title: signal
---

<div class="command">> open_channel --secure</div>

<p>Use this interface to send a direct signal to the operator. Information should be concise. Encrypted transmission is simulated.</p>

<form action="https://api.web3forms.com/submit" method="POST" class="terminal-form">
    <input type="hidden" name="access_key" value="44915114-2cd1-4085-adfa-82c13fc1151e">

    <div class="form-group">
      <label>[ORIGIN_ID]:</label>
      <input type="text" name="name" placeholder="identity_slug" required>
    </div>

    <div class="form-group">
      <label>[RETURN_PATH]:</label>
      <input type="email" name="email" placeholder="email@address.net" required>
    </div>

    <div class="form-group">
      <label>[MESSAGE_DATA]:</label>
      <textarea name="message" rows="5" placeholder="enter_logs_here..." required></textarea>
    </div>

    <button type="submit" class="nav-link">> send_signal</button>
	
	<input type="hidden" name="redirect" value="http://localhost:4000/success">
</form>

<style>
.terminal-form { margin-top: 30px; font-family: 'JetBrains Mono', monospace; }
.form-group { margin-bottom: 20px; display: flex; flex-direction: column; }
.form-group label { color: var(--red); margin-bottom: 5px; font-size: 0.8rem; }
.form-group input, .form-group textarea {
    background: transparent;
    border: 1px solid #ddd;
    color: var(--black);
    padding: 10px;
    font-family: 'JetBrains Mono', monospace;
}
.form-group input:focus, .form-group textarea:focus {
    outline: none;
    border-color: var(--red);
    background: rgba(211, 47, 47, 0.02);
}
</style>