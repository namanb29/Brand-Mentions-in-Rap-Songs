# Brand Name Dropping in Songs
![image](https://github.com/user-attachments/assets/161cf27f-0eb1-4cef-a6c1-5f6b51cfed3b)
Ever wondered how hearing your favorite brand name in a rap song might affect the company behind it? Rap music has always been about making bold statements and setting trends, and brands are often caught in the mix. From sneakers to luxury cars, you’ll hear all sorts of products mentioned in the lyrics of popular rap tracks. But does this kind of brand placement actually pay off for companies?

In this project, I’m diving into whether mentions of brands in rap music can actually help brands save money and reach to customers. It’s like exploring whether being featured in a rap song can be more than just a lyrical shout-out. Let’s find out if the rhythms and rhymes of rap music are driving more than just hits—they might be driving business as well!

I’m focusing on a select subset of songs to explore the impact of brand mentions in rap music. While there are millions of songs across genres, I’ve chosen to narrow my analysis to tracks from 10 popular rap artists who have been primarily active since the year 2000. This choice is driven by the significant role rap music plays in contemporary culture and its tendency to feature brand mentions prominently. Rap artists often use brand names in their lyrics to make bold statements, build their personas, and connect with their audience. By analyzing these high-profile artists, I aim to uncover whether their brand references translate into financial benefits for the brands mentioned.

I used python to scrape lyrics using the Genius Lyrics API via the beautifulsoup library then created separte dataframes for each artist showing the number of times certain brands were mentioned by them in their songs. A lot of times brands aren't mentioned directly but by the use of "keywords". To overcome this issue I created a dictionary to map these keywords to the respective brand names.

Undoubtedly, the most direct way to assess the impact of brand mentions would be through analyzing sales data. However, obtaining accurate and comprehensive sales data directly tied to specific brand mentions in rap music is challenging and often impractical. Instead, I will focus on alternative metrics to gauge the impact. Specifically, I’ll examine Google search trends to see if spikes in brand-related searches correlate with the release if the songs. Additionally, I’ll estimate the potential money saved by brands through these free mentions compared to traditional advertising costs. This approach will provide insights into the effectiveness of brand placements in rap music, despite the difficulties in accessing precise sales data.


# 1. Requirements
This project is developed using Python version 3.9.6. It relies on the following third-party libraries:

```
pandas
requests
re
beatutifulsoup4
seaborn
matplotlib
```


# 2. Instructions for Execution


## 2.1. Scraping Lyrics

1. Open 'scraping.ipynb` notebook.
2. Navigate to the **Retrieving URLs** section. Enter your own Genius API Token and put the name of the artist and desired number of songs in the print command to run the function and retrieve urls to the lyrics.
3. Navigate to the **Scraping Lyrics** section. Enter the url of the desired song in the print command and run the function.
4. Navigate to the **Scraping Lyrics and Saving All Lyrics in One Files** section. Enter the name of the artist and desired number of songs in the print command to run the function and save all the lyrics to a .txt file.

## 2.2. Analyzing the Lyrics

1. Open 'Main.ipynb' notebook.
2. Choose the desired selection of brands and artisits and execute all cells.


# 3. Analysis

## 3.1 # Which Brand Has the Highest Mentions?

![image](https://github.com/user-attachments/assets/3b9512d6-bf20-4b9e-8a26-baf188c13963)

The graph reveals that Gucci ranks highest in brand mentions, followed closely by various car and other luxury brands. This observation is consistent with existing research on brand mentions in rap music, which often highlights the prominence of high-end and aspirational brands.


