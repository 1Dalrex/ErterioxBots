Albion Online Trading Bot

This is a ready-made trading bot for Albion Online that automates in-game trading.
The user launches the application, configures the settings, and starts the bot.

The bot supports multiple operation modes, including updating buy/sell orders, buying items, selling items, cancelling orders, and 24/7 continuous operation.

![Bot menu](documentation/imgs/bot_menu.png)

<div style="border:1px solid #ccc; padding:10px; border-radius:8px;">
  <b>min_random_delay</b> — minimum delay between actions (seconds).
</div>

min_random_delay — Minimum Random Delay

Type: float (seconds)
Default: 0.5

Description:
This is the minimum delay between bot actions.
The bot randomly selects a delay value between min_random_delay and max_random_delay.

Purpose:
Adds randomness to bot behavior so it looks more natural and less robotic.

Example:
If min_random_delay = 0.5, the delay will never be less than 0.5 seconds.

max_random_delay — Maximum Random Delay

Type: float (seconds)
Default: 2.0

Description:
This is the maximum delay between bot actions.
The bot randomly selects a delay value between min_random_delay and max_random_delay.

Purpose:
Prevents the bot from waiting too long between actions.

Example:
If max_random_delay = 2.0, the delay will never exceed 2 seconds.

How it works together

The bot selects a random delay like this:

delay = random.uniform(min_random_delay, max_random_delay)


So if min_random_delay = 0.5 and max_random_delay = 2.0, the delay will be randomly chosen in the range:

0.5 — 2.0 seconds
