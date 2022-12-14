# Introduction

Regression Games uses Git (and more specifically GitHub) as the backbone to manage and version your bots. 
This means that we support a wide variety of ways for players to program their bots, whether it be locally or
in online IDEs such as Replit and Codespaces. This document goes over how to develop your bots.

For newer players, we recommend using Codespaces or Replit for development, so that you don't need to manage
your own development environment.

# Finding your bot code

During onboarding, you should have created a bot, backed by a GitHub repo. If you have not done this yet,
make sure to create a new bot within the [Bot Manager page](/bots).

If you are signed in and have created a bot, you can see your bot here (or in the [Bot Manager page](/bots)).

![Detailed Bot Card Component (this is only viewable within the RG Documentation Site)](rg:firstBotDetails)

Click on the GitHub link directly below your bot to see your code. The green "Code" button on GitHub will give
you access to the URLs and features to clone your repository to your local machine, or edit yor code on Codespaces.

# How development on Regression Games works

All bots on Regression Games are stored as GitHub repositories. Whenever a change to your code occurs in git, your bot's logic is automatically updated. If you bot is in a match when this update occurs, the bot will automatically disconnect, refresh its code, and reconnect to the match! This reload process happens live and automatically, and usually takes a few seconds to complete.

When creating your bot, you have the option to load your bot from a specific branch, or from a hardcoded commit. If you select a specific branch (e.g. `main`), then the bot will always pull the latest code from that branch. If you select a specific commit, the bot will never be reloaded, and will only pull the code from that specific commit. 

# Developing on Codespaces

[Codespaces](https://github.com/features/codespaces) is the fastest way to get up and running with bot development. Codespaces is the cloud IDE (based on VSCode)
from GitHub and Microsoft that allows you to edit your GitHub repositories with just a few clicks. _Please be mindful of the [usage limits for Codespaces](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces) on free GitHub accounts (~ 60 hrs free per months)._

To get started, navigate to the GitHub page for your code. Then select the "Code" button, click "Codespaces", and click "Create codespace on main".

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_start.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

A new codespace will be created, where you can edit bot code and push it to your GitHub repository.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_editor.png" alt="drawing" style="height: 400px; margin: auto; margin-bottom: 18px;"/>

Make a modification to your bot in `index.js`, such as having the bot saying something with the `bot.chat("Hello world")` method. Once you have a change, you can push (or save) your code to the GitHub repository using the Source Control button in the left-hand pane (you can also open this with Ctrl+Shift+G). Enter a message to describe your changes (e.g. "This bot now says hello") and click "Commit". There may be messages about adding unstaged changes - you can click **always** for this.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_commit.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

At this point, your changes have only been **prepared** for upload. Finally, click "Sync Changes" to save your code on GitHub. Once again, you may get a dialog, this time about where these changes are being saved - you can click "Ok, and don't show again".

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/codespaces_sync.png" alt="drawing" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

That's it! If you were to get into a match, you should see your bot load and follow your new logic. If you are in a match while do this update, you should see your bot disconnect and reconnect, at which point it will be loaded with the new code.

# Developing on Replit

[Replit](https://replit.com/) is a online IDE for developing code in a variety of languages. It features a variety of features like multiplayer editing, community templates, AI code completion, and a mobile app for programming on the go.

Once you create an account, click the Create button, and then the Import from GitHub button.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_create.png" alt="replit create" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_import.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

Then, click the **Connect GitHub** link to authenticate GitHub within Replit. Once you go through that authentication flow, wait a few seconds on Replit, and you should see the search box change to allow searching through your repositories.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_github.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

Search for your desired repository, select it, and then click "Import from GitHub".

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_select.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

**Please note that unless you paid for Replit, you will need to make sure your repository is public. If you wish to keep your repo private, you can use your own local editor and git set up to update bots. Otherwise, you can make your repo public at the bottom of the repository settings page in GitHub. If you do change your repository visibility, make sure to refresh your Replit page.**

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_privacy.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

After clicking import, you will see your code!

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_editor.png" alt="replit import" style="height: 400px; margin: auto; margin-bottom: 18px;"/>

In order to upload new code to GitHub, we need to link our GitHub information. We do this by adding secrets, or environment variables, to our Repl. Click the “lock” icon in the bottom-left tools menu to access the Secrets pane. If this is your first time using Replit, it will have a message about using Secrets for the first time. You can click “Got it”, then “Skip” and then you should see the screen below:

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_editor.png" alt="replit import" style="height: 400px; margin: auto; margin-bottom: 18px;"/>

Now, click "Open raw editor" to see a dialog to enter JSON. Here we will enter information that will be used to push our code to GitHub (and therefore Regression Games) when clicking the "Run" button at the top of your Replit editor.

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_json_entry.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

This JSON can be copied from your bot details in the Bot Manager screen. Navigate to your bot, and click the "replit Settings" button to view a copyable JSON. Note that you will need to follow the instructions in that pop up to receive a [GitHub Personal Access token](https://github.com/settings/tokens/new).

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/replit_json_info.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

Make a change to your code, and then click "Run" to push your changes! The first run may take a bit of time, and you may need to click it twice. When it asks for a commit message, put “Initial code”. Whenever you click “Run”, don’t forget to enter a message or at least just hit enter for the default timestamp message, or else your code won’t upload! You should see your console print some information about uploading this code to git.

# Developing locally

To develop bots for Regression Games locally, you will need an IDE or text editor (such as [VSCode](https://code.visualstudio.com/), [IntelliJ] (https://www.jetbrains.com/idea/), etc...), as well as [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Follow the links for each of those items if you need to install those tools.

Once you have an editor of choice and git installed, you can simply clone your repository and start editing your code. If you are logged in to Regression Games, you can see the GitHub link below your bot's title within the Bot Manager. Click this link to view the GitHub repository, which has a green "Code" button that provides links for cloning.

![Detailed Bot Card Component (this is only viewable within the RG Documentation Site)](rg:firstBotDetails)

Whenever you commit and push to this repository, the code for your bot will automatically reload. If you are new to git, you can view a getting started tutorial [here](https://www.freecodecamp.org/news/git-and-github-for-beginners/).
