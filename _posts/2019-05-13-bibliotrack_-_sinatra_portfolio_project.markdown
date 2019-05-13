---
layout: post
title:      "Bibliotrack - Sinatra Portfolio Project"
date:       2019-05-13 08:23:17 -0400
permalink:  bibliotrack_-_sinatra_portfolio_project
---

## Routes bloody routes


Despite my dramatic subheading,  my experience building an CRUD, MVC app using Sinatra was less traumatising than expected. 

The reason why I was expecting more nightmares &  frustations is that I found the Sinatra Unit a bit hard to metabolise. 
I think it was due to the labs, sometimes they were adding more confusion because they were jumping too much further or there were small mistakes and as a consequence it took me ages to complete them because I could not understand what I was doing wrong. 

Fortunately the last lab, Fwitter, allowed me to learn and understand more about this type of app and its own requirements. 

My app is called **Bibliotrack** and it allows you to manage your library by creating an account and start adding, editing and removing books at your leisure.
If you have lent some books, you can track who borrowed your book and when. 


I started by creating all the structure (folder, files, environment, gems, config.ru etc etc) and then focusing on the database. Probably I was not much focused (and  too eager to build the routes part so I rushed) and I forgot to add the column "user_id" while I was creating the table :books. Obviously when I started to build the first route and test the app with shotgun I was getting  an error. The error was located in erb :'users/show' so at first I spent a lot of time trying to figure out if I wrote the wrong code. Then I realised that on the error page, on the top right, Active Record was clearly telling me what the mistake was: **can't find "user_id" column**.  So I learned that I have to read better that page, the hints are all there! The problem was solved by simply adding a new column to my :books table.

For the last project I have a much clearer idea about my app functionality, on this occasion I have added more features *in itinere* (ongoing). I am aware that this may be not the correct procedure, however at the end it turned out well and the challenge made me learn more. 

For example, despite knowing that I wanted a feature to track lent books, I have added it only after I tested the app to see if I could add, edit or delete a book simply with an :author and :title. Then I added two columns in :books (:receiver and :date) and I build the new functionality.  Making the addition after I have already created  and edited books through tests in shotgun prooved to be time consuming, as I had realised I had to delete everything I had created previously otherwise I would encur in issues. 

Once I managed to have everthing working properly, I was very excited to try to give a nice styling to my app.
I have used Bootstrap and I found the whole process very exciting. I had so much fun finalising the layout, even if Bootstrap is quite limited.

As previously mentioned, the Fwitter lab was very useful to improve my comprehension, in particular how to  structure the code to make sure that users can edit and delete only their own resources(**current_user** helper method was definitely helpful as the name suggests!). 

My big challenge was then to start to think about what **MY APP** supposed to do and build all the functionalities according to the needs and expections of a potential user. 
*What I would like to see in the homepage? Is the app simple to use? How can I track my lent books? Can I easily edit a book? Can I see my entire library? What happen if I leave the login fields blanks?* -  Step by step I started to code to make the user experience as smoother as possible.  

So, the lesson learned is: **put yourself in the users' shoes!**

See you at the next adventure!

