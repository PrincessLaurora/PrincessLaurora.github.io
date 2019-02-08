---
layout: post
title:      "CLI Data Gem Project"
date:       2019-02-07 09:46:31 -0500
permalink:  cli_data_gem_project
---

## There is always a first time


Let's start saying that I did not realised that after the last lab of Final Projects  (Student Scraper) there was a CLI Data Gem Project, so you can imagine my face when I started to read all the Project requirements. 

I started to laugh histerically, and I am pretty sure I wasn't alone in that reaction. 

However, after doing a full immersion on Avi's Daily Deal video,  seeing  a couple of videos linked on the Resources and basically scanning World Best Restaurant project ( and other similar applications) I felt a bit releaved. 
I have followed the instructions on CLI Project In-Browser IDE Setup video and I have started to create bin and lib folders, added dependencies and  tried to understand the correct use of "require'/"require_relative".  
I won't lie, at first I felt exactly like that: 

![](https://i.kym-cdn.com/photos/images/original/000/234/765/b7e.jpg).

My main idea was to scrape a page that contained a chart and through the CLI appliction allow the user to check the entire chart, to see which item lie at a selected position and give him/her details about that item through a URL.

I changed my project 3 times (that means start all over again 3 times, yayyyy). 

My first one supposed to be an application that allows you to check the latest car safety ratings from the EURO NCAP webpage. The big issue I encounter ed was that I could not figure out how to scrape single elements! It looks easy at first but the webpage uses AngularJS Directive with ng-repeat and I did not know how to get it right! 
I have googled it  but I had no luck finding a solution.  
So I switched to another application project that allows you to check the top videogames of all times according to Metacritic. 
As soon as I was checking my first scraping attempt with **binding pry** I was welcomed by a "403 forbidden Open::HTTP” error. Thanks to Stack Overflow I found a possible solution and I have also discovered that another Flatiron student did a similar project based on Metacritic and had the same issue. 
So I followed the instructions and added the "User Agent" part to my doc variable as suggested:

`doc = Nokogiri::HTML(open("https://www.metacritic.com/browse/games/score/metascore/all/all/filtered?sort=desc", 'User-Agent' => 'chrome')`. 

This edit proved to be successful for the other student, but unfortunately despite several attemps (capitalised the first letter, changed the browser name, changed to "http"..) I still got the same error. 

I was starting to be quite frustrated so I have decided to go for another project and finally I was lucky!
*Anime Chart* is a CLI application that allows you to know the top 50 anime according to MyAnimeList website. 
You can type 'list' to see the 50 top anime chart complete with individual score. Alternatively, you can simply type a number between 1 and 50 and know immediately which anime is holding that particular position. You can also check some details about the selected anime by clicking on a link.
During this adventure I got stuck two times and I am actually feeling grateful about that because it allowed me to get a better understing of OO. I used **binding.pry** so many times to test my code and I found it so useful! There was always an hint about what I was doing wrong and summed up with the error description I could work on a solution.

At first I made quite a few mistakes on my scraping part. I started going straight away to the first element I need (getting the text of the name of the anime) but I was getting a huge array with all the anime names since the css selector was the same for each of them! So I figured out that I need to start from a parent element that contains all the names, do an iteration with **each** and then scrape again to grab the text I required.  I got the result I needed (a numbered list of anime with their individual names) but then I made another mistake...To get the other data (such as the score and the URL with the details) I was adding another two different iterations by scraping  another area of the page (oh Laura!). 
Obviously I messed up the method and at some point I was getting individual names and then the same score for everyone! 
Then I realised that I had to iterate over a  parent element that contains all the data I was looking for. I have noticed that the page was structured with 50 table rows with the same class so i did the iteration with each and from a single row I did another scraping to get the individual name, score and URL link of each anime.

Why I didn't think about that before??? 

Another mistake that I was doing was to misplace my **end**. It is so important where you place them because the return value could be quite different! And your CLI could not work how it should. 
I remember that when i realised why my CLI wasn't working (despite the fact that my scraping was accurate) and I solved the problem I felt like that for a second:

![](https://1.bp.blogspot.com/-guWNS3BNoIQ/W31YDRcRG4I/AAAAAAAAHCk/B5aTAminiXIEmDJygr8SiVzOOKw4RMwTgCLcBGAs/s1600/hackerman.jpg)


I found the CLI part easier, I have created few instance methods that will be called  according to the the input given and then worked a little bit on the visual part (I have added some colours to make it more readable).

Now that my project is done I couldn't agree more with Avi when he said that we should pratice a lot, not only by doing the labs assigned. I have all the theory I needed at hand to finish this project in less time but it took me longer than expected to metabolised it and completed it.

Long journey ahead.

See you at the next adventure! 








