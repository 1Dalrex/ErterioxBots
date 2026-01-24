<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

## 🔘 Navigation

[![Bot Settings](https://img.shields.io/badge/-Bot%20Settings-blue)](#bot-settings)  
[![Game Settings](https://img.shields.io/badge/-Game%20Settings-green)](#game-settings)  
[![How to Run the Bot](https://img.shields.io/badge/-How%20to%20Use-orange)](#how-to-run-the-bot)  
[![Logs](https://img.shields.io/badge/-Logs-gray)](#logs)

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

# Albion Online Trading Bot

This is a ready-made trading bot for Albion Online that automates in-game trading.  
The user launches the application, configures the settings, and starts the bot.

The bot supports multiple operation modes, including updating buy/sell orders, buying items, selling items, cancelling orders, and 24/7 continuous operation.

![Bot menu](documentation/imgs/bot_menu.png)

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<h2 id="bot-settings">Bot Settings</h2>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
<h3>min_random_delay</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 0.5</p>
<p>Minimum random delay between actions.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
<h3>max_random_delay</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 2.0</p>
<p>Maximum random delay between actions.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>fixed_delay</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 0.1</p>
<p>Fixed delay added to every action.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>offset_min</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1</p>
<p>Minimum mouse offset.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>offset_max</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 5</p>
<p>Maximum mouse offset.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>action_count</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1</p>
<p>How many rows/orders are processed per cycle.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>cancel_buy_every</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1000</p>
<p>Cancel BUY orders every N processed items.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>cancel_sell_every</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1000</p>
<p>Cancel SELL orders every N processed items.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>post_buy_delay</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 1.0</p>
<p>Delay after buying an item.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>min_profit_pct</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 8.0</p>
<p>Minimum profit percentage.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>tax_pct</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 6.5</p>
<p>Market tax percentage.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>check_every_lines</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1</p>
<p>Check bought items every N lines.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>take_items_batch</h3>
<p><b>Type:</b> int</p>
<p><b>Default:</b> 1</p>
<p>How many items are taken per batch.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>fallback_interval</h3>
<p><b>Type:</b> float</p>
<p><b>Default:</b> 3.0</p>
<p>Delay when an action fails.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>sell_mode</h3>
<p><b>Type:</b> string</p>
<p><b>Default:</b> single</p>
<p>How sell orders are placed.</p>
</div>

<hr>

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7;">
<h3>mode</h3>
<p><b>Type:</b> string</p>
<p>Main bot operation mode.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<h2>Game Settings</h2>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Language</h3>
  <p><b>Requirement:</b> English</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Resolution</h3>
  <p><b>Requirement:</b> 1920x1080</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Window Mode</h3>
  <p><b>Requirement:</b> Windowed</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">HUD Scale</h3>
  <p><b>Requirement:</b> 70%</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Window Scale</h3>
  <p><b>Requirement:</b> 80%</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Animations</h3>
  <p><b>Recommended:</b> Disabled</p>
  <p><b>Reason:</b> Animations can slow down the bot and cause incorrect element detection.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<h2>How to Run the Bot</h2>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <ol>
    <li>Download all files from GitHub (download the <b>.exe</b> manually, because GitHub does not include it in the ZIP archive).</li>
    <li>Run the bot once.</li>
    <li>Move all files from the created folder to:<br>
        <b>C:\Users\DALREX\Desktop\Erteriox\AlbionOnline\Trading</b></li>
    <li>Before starting the bot, make sure to select the <b>English input language</b>.</li>
    <li>Run the bot again.</li>
    <li>Configure the settings according to the instructions above.</li>
    <li>Click <b>Start</b>.</li>
    <li>Enjoy.</li>
  </ol>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<h2 id="logs">Logs</h2>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">Automatic Folder and File Creation</h3>
  <p>The bot automatically creates the required folder and files on the first run.</p>
  <p><b>Path:</b><br>
     <code>C:\Users\DALREX\Desktop\Erteriox\AlbionOnline\Trading</code></p>
  <p>If the folder does not exist, it will be created automatically after first run.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

<div style="border:1px solid #ccc; padding:15px; border-radius:10px; background:#f7f7f7; font-family:Arial, sans-serif; line-height:1.6;">
  <h3 style="margin:0 0 10px 0;">log.txt</h3>
  <p>All major errors and warnings are recorded in <b>log.txt</b>.  
     Approximately 90% of common issues are logged here, including:</p>
  <ul>
    <li>Missing files (config, items list, etc.)</li>
    <li>Incorrect file paths</li>
    <li>Missing permissions</li>
    <li>Bot UI element not found</li>
    <li>Network errors (if used)</li>
    <li>Unexpected internal errors</li>
    <li>Tesseract is not installed or not detected</li>
  </ul>
  <p>If the bot stops working or behaves incorrectly, check <b>log.txt</b> first.</p>
</div>

<hr style="border:0; border-top:1px solid #ddd; margin:15px 0;">

