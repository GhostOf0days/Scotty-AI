# Scotty-AI
Runs a LLM using the API from https://www.neuroengine.ai/. 
This is my best attempt at making a comprehensive UI for LLMs on a discord bot, similar to those found in popular webUIs. The main feature in this bot is the creation of characters, which contains a profile that is injected into the bot's system prompt. Dropdowns and modals are used to make the bot user-friendly and sleek. Characters send messages through webhooks, which contain an avatar and name for the character, so the bot can pretend to be different users during roleplay. There is also the ability to turn a character into a conversation thread, where multiple users can talk to one character in a unique discord channel. In this thread, a user can also ask another character they have made to respond to the character in the thread.

To run the bot, simply download the code and paste the token for a bot in the token file. Then give your bot manage thread, embed links, and manage webhook permissions, and run bot.py. Use the command /reload every time the bot is turned on, or when the code is updated, to sync the bot to its latest update (you do not need to restart the bot to perform updates, except for those modifying data.py, model.py, or bot.py). Be warned that restarting the bot will result in loss of user data. To alleviate this, all commands will dump the character profile whenever it is created/edited so it can be found through discord's message search feature, unless the message or channel is manually deleted. Additionally, after restarting the bot it is recommended to use /purge_webhooks to make sure there arent't leftovers from the previous bot instance (which will make it so the bot can't send a message due to discord limitations).

To use the bot, either use /help to get a list of commands (the commands are self explanatory), or ping the bot to talk.

Warning:
Editing the system prompt as this bot does will significantly decrease both alignment and truthfulness. The content generated may be wrong, toxic, biased, or harmful. As with any LLM, nothing AI generated should be taken seriously, at least without significant fact checking. You, and you alone are liable for the outputs the AI models generate.


To get started run ```pip install -r requirements.txt``` to install the dependencies. Then, add the Discord bot token to a .env file. Finally, run ```python bot.py```.