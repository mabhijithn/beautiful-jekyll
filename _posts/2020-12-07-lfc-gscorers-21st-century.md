---
layout: post
title: Liverpool goal scorers in 21st Century
subtitle: Visualizing the impact of their goals on Liverpool games
share-img: /assets/img/path.jpg
tags: [datascience, visualization,football]
---

Liverpool football club has seen great goal scorers in the 21st century. From Michael Owen's fast burning rise and fall to Mohamed Salah's Liverpool kingdom. However, whose
goals have had the most impact on Liverpool's English Premier League games? In terms of changing the state of the game- a draw to a win, trailing to catching up. Or helping LFC win all three points when they were set to win only one.

With this question in mind, I started my data visualization experiment and immediately got stuck, because, there was no data!

Oh! There is data. But not easily available for the common man. Definitely not in a structured format. There are tremendous websites like [LFC History](https://lfchistory.net/) which gives you details from
every single match that Liverpool has ever played. However, if one wanted to know "Which LFC player has scored the most goals in the last 10 mins at Anfield in the 21st century?"? There was no easy way to get hold of a structured database to answer such a question.

Since the internet is vast and full of possibilities, I set to work. With the help of few lines of code in python, the awesome tool of [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
and persistence I built a database. The story of building this database is for another day. Suffice to say, I created a structured database containing **_all the goal events:their time and name of goal scorer, of every English Premier League fixture since 2000 to 2019-2020 season_**.

With this data in my hands (on computer, of course), I charted my next path. Creating metrics that would help me analyze the impact of goals. I started with the basic attribute of **Goals per 90 minutes**. The attribute is clean enough, easily interpretable and has no bias towards players who played a lot. Next, I tried to quantify how much points a goal, thereby the goal scorer, won for Liverpool.
If a goal was the final goal in a game and it was the game-defining goal, i.e. leading to a draw or a win, the player was awarded **+1** or **+3** points respectively. The points won by a player 
was normalized by **dividing by (3 X number of appearances)**, since you can win maximum 3 points in a league game. 
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="/assets/plotly/lfcGS_pts_gp90.html" height="525" width="100%"><\iframe>
