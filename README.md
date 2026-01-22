# Albion Online Trading Bot

This is a ready-made trading bot for Albion Online that automates in-game trading.  
The user launches the application, configures the settings, and starts the bot.

The bot supports multiple operation modes, including updating buy/sell orders, buying items, selling items, cancelling orders, and 24/7 continuous operation.

![Bot menu](documentation/imgs/bot_menu.png)

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">
  
<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">min_random_delay — Minimum Random Delay</h3>
  <p><b>Type:</b> float (seconds)<br>
     <b>Default:</b> 0.5</p>
  <p><b>Description:</b><br>
     This is the minimum delay between bot actions. The bot randomly selects a delay value between <b>min_random_delay</b> and <b>max_random_delay</b>.</p>
  <p><b>Purpose:</b><br>
     Adds randomness to bot behavior so it looks more natural and less robotic.</p>
  <p><b>Example:</b><br>
     If <b>min_random_delay = 0.5</b>, the delay will never be less than 0.5 seconds.</p>

  <hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

  <h3 style="margin:0 0 10px 0;">max_random_delay — Maximum Random Delay</h3>
  <p><b>Type:</b> float (seconds)<br>
     <b>Default:</b> 2.0</p>
  <p><b>Description:</b><br>
     This is the maximum delay between bot actions. The bot randomly selects a delay value between <b>min_random_delay</b> and <b>max_random_delay</b>.</p>
  <p><b>Purpose:</b><br>
     Prevents the bot from waiting too long between actions.</p>
  <p><b>Example:</b><br>
     If <b>max_random_delay = 2.0</b>, the delay will never exceed 2 seconds.</p>

  <hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

  <h3 style="margin:0 0 10px 0;">How it works together</h3>
  <p>The bot selects a random delay like this:</p>
  <pre style="background:#fff; padding:10px; border:1px solid #ddd; border-radius:8px;">
delay = random.uniform(min_random_delay, max_random_delay)
  </pre>
  <p>So if <b>min_random_delay = 0.5</b> and <b>max_random_delay = 2.0</b>, the delay will be randomly chosen in the range:</p>
  <p><b>0.5 — 2.0 seconds</b></p>
</div>
