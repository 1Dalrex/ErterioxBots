# Albion Online Trading Bot

This is a ready-made trading bot for Albion Online that automates in-game trading.  
The user launches the application, configures the settings, and starts the bot.

The bot supports multiple operation modes, including updating buy/sell orders, buying items, selling items, cancelling orders, and 24/7 continuous operation.

![Bot menu](documentation/imgs/bot_menu.png)

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">
  
<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h2 style="margin-top:0;">Configuration Parameters</h2>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">min_random_delay — Minimum Random Delay</h3>
    <p><b>Type:</b> float (seconds)<br>
       <b>Default:</b> 0.5</p>
    <p><b>Description:</b><br>
       Minimum delay between bot actions. The bot randomly selects a delay value between <b>min_random_delay</b> and <b>max_random_delay</b>.</p>
    <p><b>Purpose:</b><br>
       Adds randomness to bot behavior so it looks more natural.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">max_random_delay — Maximum Random Delay</h3>
    <p><b>Type:</b> float (seconds)<br>
       <b>Default:</b> 2.0</p>
    <p><b>Description:</b><br>
       Maximum delay between bot actions. The bot randomly selects a delay value between <b>min_random_delay</b> and <b>max_random_delay</b>.</p>
    <p><b>Purpose:</b><br>
       Prevents the bot from waiting too long.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">fixed_delay — Fixed Delay</h3>
    <p><b>Type:</b> float (seconds)<br>
       <b>Default:</b> 0.1</p>
    <p><b>Description:</b><br>
       A constant delay added between actions regardless of random delay.</p>
    <p><b>Purpose:</b><br>
       Ensures a stable base delay for all actions.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">offset_min — Minimum Mouse Offset</h3>
    <p><b>Type:</b> int (pixels)<br>
       <b>Default:</b> 1</p>
    <p><b>Description:</b><br>
       Minimum random mouse cursor offset for clicks.</p>
    <p><b>Purpose:</b><br>
       Makes clicks look more human by shifting cursor slightly.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">offset_max — Maximum Mouse Offset</h3>
    <p><b>Type:</b> int (pixels)<br>
       <b>Default:</b> 5</p>
    <p><b>Description:</b><br>
       Maximum random mouse cursor offset for clicks.</p>
    <p><b>Purpose:</b><br>
       Limits the maximum shift for cursor movement.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">mode — Operation Mode</h3>
    <p><b>Type:</b> string<br>
       <b>Default:</b> Update Buy Orders</p>
    <p><b>Description:</b><br>
       Bot operation mode. Choose from the available modes in the UI.</p>
    <p><b>Purpose:</b><br>
       Defines what actions the bot will perform.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">action_count — Actions Count</h3>
    <p><b>Type:</b> int<br>
       <b>Default:</b> 1</p>
    <p><b>Description:</b><br>
       Number of update/sell actions the bot performs per cycle.</p>
    <p><b>Purpose:</b><br>
       Controls how many items/orders are processed each loop.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">cancel_buy_every — Cancel BUY Every X Lines</h3>
    <p><b>Type:</b> int<br>
       <b>Default:</b> 1000</p>
    <p><b>Description:</b><br>
       Cancels BUY orders every specified number of lines in the list.</p>
    <p><b>Purpose:</b><br>
       Periodically clears outdated buy orders.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">cancel_sell_every — Cancel SELL Every X Lines</h3>
    <p><b>Type:</b> int<br>
       <b>Default:</b> 1000</p>
    <p><b>Description:</b><br>
       Cancels SELL orders every specified number of lines in the list.</p>
    <p><b>Purpose:</b><br>
       Periodically clears outdated sell orders.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">post_buy_delay — Post-Buy Delay</h3>
    <p><b>Type:</b> float (seconds)<br>
       <b>Default:</b> 1.0</p>
    <p><b>Description:</b><br>
       Delay after purchasing an item.</p>
    <p><b>Purpose:</b><br>
       Allows time for the game to process the purchase.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">min_profit_pct — Minimum Profit Percentage</h3>
    <p><b>Type:</b> float (%)<br>
       <b>Default:</b> 8.0</p>
    <p><b>Description:</b><br>
       Minimum required profit percentage for a trade to be executed.</p>
    <p><b>Purpose:</b><br>
       Prevents low-profit trades.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">tax_pct — Market Tax Percentage</h3>
    <p><b>Type:</b> float (%)<br>
       <b>Default:</b> 6.5</p>
    <p><b>Description:</b><br>
       Market tax percentage used in profit calculation.</p>
    <p><b>Purpose:</b><br>
       Ensures profit is calculated correctly after taxes.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">check_every_lines — Check Bought Every X Lines</h3>
    <p><b>Type:</b> int<br>
       <b>Default:</b> 1</p>
    <p><b>Description:</b><br>
       Checks bought items every specified number of lines.</p>
    <p><b>Purpose:</b><br>
       Periodic verification to prevent errors or missed items.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">take_items_batch — Take Items Per Batch</h3>
    <p><b>Type:</b> int<br>
       <b>Default:</b> 1</p>
    <p><b>Description:</b><br>
       Number of items the bot collects in one cycle.</p>
    <p><b>Purpose:</b><br>
       Controls batch size for item collection.</p>
  </div>

  <div style="margin-bottom:15px;">
    <h3 style="margin:0 0 8px 0;">fallback_interval — Fallback Interval</h3>
    <p><b>Type:</b> float (seconds)<br>
       <b>Default:</b> 3.0</p>
    <p><b>Description:</b><br>
       Delay time when an error or fallback situation occurs.</p>
    <p><b>Purpose:</b><br>
       Gives the bot time to recover from issues or unstable states.</p>
  </div>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">
