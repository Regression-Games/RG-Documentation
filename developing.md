# Introduction

Regression Games uses Git (and more specifically GitHub) as the backbone to manage and version your bots. 
This means that we support a wide variety of ways for players to program their bots, whether it be locally or
in online IDEs such as Replit and Codespaces. This document goes over how to develop your bots.

For newer players, we recommend using Codespaces or Replit for development, so that you don't need to manage
your own development environment.

## Finding your bot code

During onboarding, you should have created a bot, backed by a GitHub repo. If you have not done this yet,
make sure to create a new bot within the [Bot Manager page](/bots).

If you are signed in and have created a bot, you can see your bot here (or in the [Bot Manager page](/bots)).

![Detailed Bot Card Component (this is only viewable within the RG Documentation Site)](rg:firstBotDetails)

Click on the GitHub link directly below your bot to see your code. The green "Code" button on GitHub will give
you access to the URLs and features to clone your repository to your local machine, or edit yor code on Codespaces.

## How development on Regression Games works

All bots on Regression Games are stored as GitHub repositories. Whenever a change to your code occurs in git, your bot's logic is automatically updated. If you bot is in a match when this update occurs, the bot will automatically disconnect, refresh its code, and reconnect to the match! This reload process happens live and automatically, and usually takes a few seconds to complete.

When creating your bot, you have the option to load your bot from a specific branch, or from a hardcoded commit. If you select a specific branch (e.g. `main`), then the bot will always pull the latest code from that branch. If you select a specific commit, the bot will never be reloaded, and will only pull the code from that specific commit. 

## Developing on Codespaces

Codespaces is the fastest way to get up and running with bot development. Codespaces is the cloud IDE (based on VSCode)
from GitHub and Microsoft that allows you to edit your GitHub repositories with just a few clicks.

To get started, navigate to the GitHub page for your code. Then select the "Code" button, click "Codespaces", and click "Create codespace on main".

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_start.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

A new codespace will be created, where you can edit bot code and push it to your GitHub repository.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_editor.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

Make a modification to your bot in `index.js`, such as having the bot saying something with the `bot.chat("Hello world")` method. Once you have a change, you can push (or save) your code to the GitHub repository using the Source Control button in the left-hand pane (you can also open this with Ctrl+Shift+G). Enter a message to describe your changes (e.g. "This bot now says hello") and click "Commit". There may be messages about adding unstaged changes - you can click **always** for this.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_commit.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

At this point, your changes have only been **prepared** for upload. Finally, click "Sync Changes" to save your code on GitHub. Once again, you may get a dialog, this time about where these changes are being saved - you can click "Ok, and don't show again".

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_sync.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

That's it! If you were to get into a match, you should see your bot load and follow your new logic. If you are in a match while do this update, you should see your bot disconnect and reconnect, at which point it will be loaded with the new code.

## Developing on Replit

## Developing Locally

To develop bots for Regression Games locally, you will need an IDE or text editor (such as VSCode, IntelliJ,
etc...), as well as git. Follow the links for each of those items if you need to install those tools.

Once you have an editor of choice and git installed, you can 
