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

## 3.1 Which Brand Has the Highest Mentions?

![image](https://github.com/user-attachments/assets/3b9512d6-bf20-4b9e-8a26-baf188c13963)

The graph reveals that Gucci ranks highest in brand mentions, followed closely by various car and other luxury brands. This observation is consistent with existing research on brand mentions in rap music, which often highlights the prominence of high-end and aspirational brands.

## 3.2  Which Artist Had the Highest Mentions?

![image](https://github.com/user-attachments/assets/ba67d4a3-8444-4dc9-9c82-e4773cc89741)

Among the 10 popular rap artists considered, Kanye West stands at the top of the list with the highest number of brand references (106) mentioning Louis Vuitton 22 times in the 100 songs that were part of our data set. 

## 3.3 What was the Impact?

### 3.3.1 Google Searches

Let's take a look at the google search trends history of Louis Vuitton.

![image](https://github.com/user-attachments/assets/6e03c28a-a23f-417a-8936-4423a79e74e1)

I have marked special pointers representing release of a song or any other event relating to the brand. Despite being extremely popular songs, both Gold Digger and Stronger by Kanye West, did not really cause any manjor increase in LVs google search interest score. However, we should consider that fact when these songs were released, internet access was still very limited in most parts of the world. If we look at the data a decade later we can see that the release of Eminem's Godzilla increased LVs search interest score an additional 16 points. Furthermore, when LV announced the release of their documentary on the occasion of the 200th birhtday celebrations of their founder, their search interest score skyrocketed and reached an all time high. 

### 3.3.2 Financial Impact
As mentioned earlier, the lack of direct sales data makes it difficult to measure the financial impact of brand mentions in rap music. To address this, I’ve turned to another key metric: Cost Per Mille (CPM). CPM refers to the cost a brand incurs for every thousand impressions their advertisement receives. It’s a common metric used in advertising to gauge the efficiency and reach of promotional efforts. In this project, I’ve scraped CPM rates from Gupta Media, which provides a comprehensive overview of average rates for various platforms. However, it’s important to note that the rates I’ve used are specific to the U.S. market. By comparing these CPM rates to the value of brand mentions in rap lyrics, we can estimate the potential savings brands might achieve through these organic placements.

![image](https://github.com/user-attachments/assets/ab51cd93-cb0a-4d05-a577-27000df1e3a2)

We can see that CPM rates vary significantly across different platforms. For instance, according to the data from Gupta Media, the average CPM on Facebook is around $6.99, while on YouTube, it’s notably lower at approximately $3.07. This means that for every 1,000 impressions, a brand would typically spend $6.99 on Facebook to reach its audience, compared to just $3.07 on YouTube. These differences highlight how the cost of reaching consumers can vary depending on the platform. By understanding these rates, we can better estimate the financial value of brand mentions in rap music. We'll be using the average of the CPM of all four platforms which is $4.19 for the purpose of ease.
Let's look at a few examples to give us a clearer picture: 

- Post Malone's **Wow** has been streamed 1,715,833,131 times so far on spotify. This song has referenced Mercedes Benz (G-Wagon), McLaren (720S) and Lamborghini (750 Lambo). To find the value of these mentions in monetary terms we simply divide the number of streams by a thousand and multiply that by the CPM rate. So if either of the three brands wanted to gain 1,715,833,131 impressions on the aforementioned social media platforms they would have had to pay approximately **$7,189,340** based on the 2024 CPM rates. If we just look at the youtube streams, the official music video of the song has been streamed 336,590,802 times so far while the official audio has been streamed 5,461,252 times making it a total of 342,052,052 streams on youtube. If we consider the youtube CPM of $3.07, these luxury car brands have saved approximately **$1,050,099** each in brand marketing!

- **Fashion Killa** by A$AP Rocky with 279,500,631 streams on spotify helped brands like Balenciaga, Dior, Prada, Dolce and Gabbana etc., mentioned in this song, save just over **a million dollars** each in paid social media marketing.

- The popular song **Gucci Gang** by Lil Pump has 651,057,082 streams on spotify so far resulting in alomst **3 million dollars** in savings!

However, what must be noted here is that the CPM rates that I considered here are specific to the US. These will differ according to geographical regions as well. Furthermore, another interesting point is that I have only taken into account the number of streams on spotify. These songs are played on other platforms like apple music, youtube music etc., live artist shows, radio channels, pubs, cafes etc. If one somehow manages to collect streaming data from all the possible sources and calculates the financial value of the brand mentions in these songs, the figure would probably be 10 times that of the ones I calculated above.

In some cases, such brand mentions have also led to collaborations between artists and the brands. For example, Drake and Travis Scott successfully collaborated with Nike to introduce their own line of clothing and shoes. Travis Scott also collaborated with McDonald's to introduce a customized menu option "Travis Scott Meal". Kanye West had a long running partnership with Adidas for his extremely popular shoe line Yeezys. Kanye West expanded the Yeezy fashion line by another collaboration with GAP. Another popular collaboration was that between Cardi B and Balenciaga when they made her the face of their winter campaign in 2020 and most recently she made her debut at the Balenciaga Los Angeles Fashion Show in 2023.
