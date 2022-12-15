# Introduction

Welcome to Regression Games, the ultimate AI gaming platform!

# Overview of Regression Games

Regression Games is an AI gaming platform that allows players to write artificial intelligence and code to compete against each other in various games and competitions. Our platform offers a wide range of features that make it easy for players of all experience levels to participate and enjoy this innovative way of playing games.

<iframe width="560" height="315" src="https://www.youtube.com/embed/JUQLkHKeocI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen style="margin: auto; margin-bottom: 18px;"></iframe>

Our platform is designed to provide a fun and engaging way for players to explore the world of AI and code. Whether you are a seasoned coder or a beginner, Regression Games offers a unique and exciting way to learn, play, and compete.

# How to play

Regression Games provides a variety of game modes to choose from, such as practice mode and battle modes. Players create bots using JavaScript (roadmap for other languages coming soon) and an [editor of their choice](/documentation/developing) to compete in the [Ultimate Collector](#season-0-ultimate-collector) challenge. Players can create bots on their Regression Games account and update their code and strategies in real-time. Bots are managed using [Git](https://git-scm.com/) (don't worry if you haven't used Git, we manage all of that for you), and code changes are automatically reloaded in-game. Edit and iterate on bots to create the best strategy and work your way up the leaderboard!

<img src="https://raw.githubusercontent.com/Regression-Games/RG-Documentation/main/images/code_example.png" alt="replit import" style="height: 350px; margin: auto; margin-bottom: 18px;"/>

You can learn more about developing bots by taking a look at our [Developing page](/documentation/developing) and our Minecraft AI library, [rg-bot](/documentation/rg-bot).

# Requirements to play

The first game that players will build AIs for is **Minecraft**. Playing requires a valid [Minecraft account](https://www.minecraft.net/en-us/store/minecraft-java-bedrock-edition-pc) and a Java version of Minecraft. Players will need to install and play on Minecraft version 1.18.2, which can be installed using the [Minecraft Launcher](https://www.minecraft.net/en-us/store/minecraft-java-bedrock-edition-pc).

You will also need a [GitHub account](https://github.com) to store bot code. Your GitHub profile can be connected to your Regression Games account within the profile page.

# Season 0: Ultimate Collector

Ultimate Collector is a **Minecraft scavenger challenge**. The goal of the challenge is to be the first team to reach the target score. Points are gained by collecting certain items in the Minecraft world. The match ends when a team reaches the target score, or when the 15-minute time limit is reached. The team with the highest score at the time limit wins! The target score is 50 points per team member. In a 2v2 game, the target is 100 points. In a 4v4 game, the target is 200 points.

Players play on a team that consists of themselves and bots that they have programmed. Practice Mode allows a player to create a team with one bot and play without an enemy team or time limit. 2v2 Mode pits one player and their bot against another team. 3v3 Mode pits one player and two of their bots against another team.

The Ultimate Collector challenge uses a static seed where the player will spawn in a village near the starting bell. Try it out yourself in single-player mode: `109513178`. You can start exploring for cool items and structures for your bot to interact with (hint: check out coordinates (x=50, z=50) for some loot).

## Point values

Various items in the Minecraft world are worth points towards your team. Points are obtained by holding items in the inventory of a player on your team. 

| Point Values | Items                                                                                                                  |
|--------------|------------------------------------------------------------------------------------------------------------------------|
| 1 Point      | Rabbit_Hide, Apple, White_Wool, Black_Wool, Brown_Wool, Gray_Wool, Leather, Chicken, Porkchop, Poppy, Coal, Sugar_Cane |
| 3 Points     | Shroomlight, Iron_Ingot, Rabbit_Foot                                                                                   |
| 5 Points     | Bread, Paper, Emerald                                                                                                  |
| 15 Points    | Bell, Compass, Golden_Apple                                                                                            |
| 30 Points    | Magma_Cream, Gilded_Blackstone                                                                                         |
| 100 Points   | Ancient_Debris                                                                                                         |