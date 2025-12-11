# Foundations final project: _Steam Sales Monitor_
This project is my final project for a class I have taken in Columbia Journalism School's data journalism program called **"Foundations of Computing"**, instructed by Jonathan Soma. This project includes two interactive graphs, updates every two hours, that visualize dataset from CheapShark, and inform the readers what they should expect and look at from a discount page on Steam when looking at deals.

## _What I want to accomplish_
I want to use this page to tell a few key factors inside the Steam games deal dataset, and the best games to buy are not only limited on the algorithm that Steam will show on the website. There are interesting aspects, such as release year, sale price, and deal rating to look into.<br>

I want to also show my readers what do they expect from the game industry by year, how many new games are there, and how much are they when on sale. I think this could be a snippet of the industry, one that helps us understand how pricing, popularity, and player expectations have evolved over time.<br>

By looking at release year, sale price, discount percentage, and deal rating together, we can start to see patterns: older titles that are still highly rated and heavily discounted, newer games that rarely go on sale, and mid-tier games that might be the real “best value” even if Steam’s algorithm doesn’t push them to the front page.<br>

This isn’t meant to be a full market report, but rather a small, data-driven snapshot of the PC game industry viewed through the lens of discounts. If you’re a player, it can help you spot better deals than what the storefront automatically recommends. And if you’re just curious about the industry, it offers a quick way to see how crowded each year is with new releases, and what kind of prices you can expect when those games finally go on sale.

## _Skills and approaches_
I have tried a few news things and incorporated some existing knowledge I have in computing when doing this project.
### 1. Pitching 
In the early stage of this project, I had a few ideas of what dataset I should play with. As a result, I thought about doing a data visualization in the game industry and sale market because I'm a video game consumer, as well as a player myself. I always go to Steam store to find games that are interesting and in a good price. Yet, I usually come across the difficulties where I cannot find the perfect game to buy. Because the Steam store's page is only valuing good or bad reviews, which is their only rating system, and it often shows you the most popular games on the front page, so I think there might be a dataset behind it that could filter everything in a better way.<br>

I came across to steamdb.info, https://steamdb.info/, which is a very complete and popular database that generated from Steam's API. I immediately started to scrape this website and tried multiple ways to get the database. However, this website is under a strong protection that you will NEED to ask permission to get the database, otherwise you'll be blocked by Cloudflare each time you try to access the CSV file you get at the end.<br>

### 2. Refining

I first scraped with requests and BeautifulSoup, it blocks me right away. I then tried PlayWright, it worked fine in my Jupyter notebook. But since this assignment is all about to build an auto-updating website to visualize a dataset, my plan is to create a workflow on GitHub that updates me the website every two hours. <br>

When I put that workflow to run, the workflow started to fail each time I run it. I finally fixed it by changing my code a few times, for example like a Timeout error I will change the run time. At the end, this worked fine when I have the workflow to run, but when I looked at the CSV file I got on GitHub, the file is completely blank and empty. <br>

I brought this to my professor and he tried to troubleshoot with me to see what is wrong, turns out that when we let the code screenshot the web page we get when we do the scraping, it shows a "verifying if you're a robot" bar powered by Cloudflare and it's not proceeding to show the front page of SteamDB. So I decided to change to another database, where I found CheapShark https://www.cheapshark.com/. <br>

This database has multiple different game shops, but it appears that their Steam database is still approachable for me to finish my project. So I started to think what I can do with this database, and I end up have the ideas of comparing sale prices vs. year, as well as show top 20 games.

### 3. Technical skills 
Scraping through PlayWright, writing and designing html, workflow on GitHub.

### 4. What I grew the most
Better scraping, better html building, and first time building a web page ever!

## _What I can do better_
1. I can try my hardest to get the SteamDB dataset... in what way I don't know, maybe request the dataset, get in touch with them...? Cause it is a so much better database & website. But I'm on a deadline and I feel like it will take so much longer to wait for their response so I gave it up. Luckily I found another website.
2. I can design the web a little bit better? I don't know how to design a web to be honest, so a lot of it is just based on vibes I feel what a web page should be. I don't have the skill to properly design a web page, so this is the best I can do.
3. I can refine the story angle a little bit better...
4. I can graph my charts a little bit better, with annotations and other stuff.

