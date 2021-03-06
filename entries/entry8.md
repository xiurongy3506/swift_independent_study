# Entry 8: MVP + a little more than MVP  
This week I was able to get my MVP done, use firebase pre-built login, and expand on the features in the timer section of the app. Read and find out how I did that!

## Fixing the bug from last week: String to Integer
Last week, I was having trouble passing on data from a string to an integer. After many attempts in changing the variables around, I decided to use force unwrapping to convert the string to an integer. In this case, it worked as the second is able to be recognized as an integer. 
<p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/sec.png"/>
</p>   

## MVP
The day before the SEP EXPO, I was rushing to get my MVP done. Since Jennifer was introduced to Firebase last week, I figure that having a messaging app done will be unrealistic. As a result, I decided to focus solely on the timer and the to-do list part of the app as of now.   

:point_right: **Here is what I have for MVP**  
_The beeping sound effect cannot be heard because the following is a gif_
 <p align="center">
        <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/mvp.gif?raw=true"/>
    </p>  

## Firebase log in   
As you can see in my MVP, the username and password were entered assuming that the user has an account, but the "create an account" function does not work yet. As a result, I decided to find the easiest way to allow the user to create and login into their account using **a pre-built UI from Firebox.**
  
:sparkles: **Shout out to Jennifer who has the Firebase for the Productivity app set up** because the connection setup process for Swift and Firebase can take forever. :sparkles:   

#### How did I do that?
1. I read over the [documentation](https://firebase.google.com/docs/auth/ios/firebaseui) for adding sign-in to your iOS app with FirebaseUI.  
2. I looked at the comment below the video [Code with Chris on how to build a login page](https://www.youtube.com/watch?v=brpt9Thi6GU)   
     - Before watching the video, I tend to sort the comment by the "Newest." This makes sure that I am able to see the recent comment, but also understand if the video is up to date to the version of Swift or Firebase that I am using.   
     - The **comments** below the video are VERY USEFUL because sometimes it gives you **updates** on the video content. Since the video is made in 2018, and Firebase is constantly updating their code and system, there are certain ERRORS that you will encounter if you follow along with the video exactly. 
3. I downloaded the necessary pod files.   
4. I watched and followed along the part of the tutorial that I needed.   
     - Note: I did not watch every single part of the tutorial because there are certain parts that I already know (for instance, setting up Cocoapods), so I skipped to the part that teaches me how to use the code to set up the email authentication.   
5. I run and tested my app. 

#### Why use pre-built UI from Firebase?  
The pre-built UI  

:star: directs you to create an account if Firebase recognizes that you are a new user.  

<p align="center">
    <img width = 50% src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/create.png"/>
</p>
:star: allows you to log in if your account has already been created   

<p align="center">
    <img width = 80% src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/existing_user.png"/>
</p>
:star: stores all the user information in Firebase  

<p align="center">
    <img width = 80% src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/users.png"/>
</p>  

Because the pre-built UI includes a lot of the features for you, it will save you some time from creating all the login/create an account features in swift and then connecting each information piece to the Firebase Database.   

## Notifications and UI Alerts
How did notification come to my mind all of a sudden? Well, when I was thinking about making my Timer more like a Pomodoro timer, I thought about using a notification to remind the user about the timer they set and hopefully get them back to the app.   

The purpose of the timer is to make sure the user is using the time they set productivity and staying away from any distractions of the phone. Therefore, I decided to notify the user and call them back to the app once the user leaves the timer page (In this case, it is under the circumstance that the timer is set and counting down)    

Three different resources that have helped me make my Notification buttons: 
- [If you are a video person, definitely follow along with Code with Chris](https://www.youtube.com/watch?v=JuqQUP0pnZY )
- [Super useful for referencing back, and understand parts of the code](https://useyourloaf.com/blog/local-notifications-with-ios-10/)
- [Not all the parts of the code work for me, but some of the comments on the code are useful](https://www.appcoda.com/user-notifications-ios12/)


### What if the notification doesn't work for the user?  
Well, this means the user is very distracted, so once they go back to the app, an alert will pop up, asking the user why they quit the app. This is meant to make the user feel guilty and reflect. Hopefully, by writing down the reason why he/she is not productive, the user can become more productive the next time.    

- [This teaches you how to make different types of UIAlertController](https://learnappmaking.com/uialertcontroller-alerts-swift-how-to/)

## A Basic timer -> A Focus timer    
After applying all the features I added, I was able to make my timer a bit more like a focus timer.  
Here are some of the current features  
1. The user can set certain **minutes** they want to stay productive 
2. The user **can not go back** to other screens/views with the app once the timer is set 
    - _I got rid of the <Back button during the countdown interval_
3. A beeping **sound** will occur when the time is up to notify the user     

**When the time is counting down and the user quits the app,**
4. A **notification** will pop up calling the user back to the app  
    - the notification has a sound by the way 
5. An **alert** will appear when the user returns to the app  

:point_right: **Here is a demo of all of the above features** 
  <p align="center">
        <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/advanced_timer.gif?raw=true"/>
    </p>    
    
## Takeaways  
1. **Be proud and passionate with the projects you created** It's been week 8 since I've been doing independent study, and I couldn't express how happy enough I am by having a Minimum Viable Product done. It is not easy to get to this far and have something done, so be proud of your self. What kept me going from an MVP was a passion, I wanted to make this time even better, so I continued to learn and add on to my app.   
2. **Invest in the process.** Sometimes the results are not always as important as the process. For instance, it always takes me longer to research and figure out how to debug (even from last week) than to simply write down the code that works. By investing in the process, it teaches me how to think and arrive at the solution. By writing this blog entry, it helps me recap the process (i.e. steps on how I learn the notification part of the timer).
   
