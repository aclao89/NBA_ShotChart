# NBA_ShotChart

Inspired by Naveen Venkatesan, I took up the task of learning how to make a basic
NBA Shot Chart using a Python package called "nba_api". The National Basketball Association (NBA) has used data and analytics to assess performance and formulate game plans. Daryl Morey, General Manager of the Houston Rockets from 2007-2020, is considered to be one of the fathers of the modern-day NBA analytics movement who built a Rockets team suited to knock off the dominate shooting duo in Golden State. However, the Rockets became the victim of their own analytics on May 28th, 2018 by missing [27 consecutive 3-point](https://www.nbcsports.com/bayarea/warriors/odds-rockets-missing-27-straight-3-pointers-vs-warriors-was-insane) attempts in their Game 7 loss.

Analytics is here to stay and provides rich insight to maximize performance but team chemistry (maybe some luck) is something that is not quantifiable (yet) and beyond the scope of this analysis but I digress. Let's hop into the fun stuff!

## Where do I even start?
### Data Source: NBA API

I came across tons of player shot charts but gathering data can be a daunting task. Each of the 30 teams play 82 games in the regular season and 16 teams move onto the post-season to reach the coveted Larry O' Brien trophy. The amount of data generated is staggering! Luckily, the NBA made extracting and using the data easy through their own package - "nba_api". The [documentation](https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/examples.md) details on how to use the package to collect statistics from stats.nba.com

The NBA’s API (application programming interface) provides a whole variety of data and player information. This data is a result of some of the newest technology with player tracking and information management, which provides a great backing for how information is collected by the NBA and teams.

The NBA API provides shotchartdetail within ShotChartDetail that will return a DataFrame with the X and Y coordinates of all the shots taken by a player you are requesting. These X and Y coordinates can be plotted in a scatter plot, which when overlaid on a court will result in your final shot chart.
## What is an NBA shotchart?

A shotchart is a type of visualization that allows coaches and players to assess strong
and weak points of a player's shot selection. These charts give coaches an idea
of how effective a player's offensive capabilities can be in certain areas on the court.
With a little bit of frequency analytics, coaches can devise plays based on where players are making the most shots, which can allow players to be more effectively utilized in a game.

### Components of shotchart

A shot chart contains two layers. The bottom (first) layer is a picture of the drawing of a basketball court. The top (second) layer is a scatterplot of the shot locations. Once these two overlap, we can visually see those shots as dots over a half court.
