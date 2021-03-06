# Entry 6: Debugging + Combining Parts
Previously, I have been working on parts of the app (i.e button click, timer, setting up views... ), and last week, I was struggling with passing on data from one view to another. Time has gone by so fast, and I'm already writing Entry 6. With that said, I have to speed up a little and have my Minimum Viable Product done by Friday. Therefore, for this week, I started combining some mini parts of the project that I have worked on into one. 

## Debugging
Last week, I have faced a huge challenge in passing on data. What was really challenging for me to learn swift on myself was that most of the video tutorials I watched were mostly for Swift 8, Swift 3 and other versions, so sometimes when I code along, I would get unexpected errors that I do not know how to fix. After fixing all the bugs, I truly realize how glad I was to know someone who actually knows Swift. 

#### :star: Help from John
John was previously introduced in Entry 2, my co-worker who introduced me to Cocoapods. While I was not able to see him last week, I communicated with him through Slack and he was able to modify parts of my code to make it work. I took a look at the code he wrote and compared to the one I wrote last week. In order to fully understand where my mistakes were, I created another same project to test my understanding. 

The error below indicates that the **app crashes due to the failure to access something**. What's really tricky about this error is that you do not know where the failure is at specifically, so you would have to look over your code to find it. 
 <p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/signal.png"/>
    </p> 

### The bugs in my program:   

1. I used a Swift class instead of Cocoa Touch class.  
    **-> Cocoa Touch Class** generates interface builder files for me while for Swift Class, I have to type in the starting codes. While there isn't a big difference between the classes, I might get errors typing the code myself using Swift Class.  

    <p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/class.png"/>
    </p> 
    
2. There were multiple connections to the submit button  
    **->** Go to the connection inspector and make sure there is only one view controller option. Close up connections by clicking "x" if there are more than one connection.  
    **Here's how it should look:**

    <p align="center">
    <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/connection.png"/>
    </p> 
3. A segway was not able to be made from one view to the other because I did not give the segway an identifier in the identity inspector.  
    **->** Make sure what I have written in code is consistent with the identity inspector.

     <p align="center">
        <img src = "https://raw.githubusercontent.com/xiurongy3506/swift_independent_study/master/img/identify.png"/>
     </p> 

#### Data passed Successfully :satisfied:  
A demo of passing user input from one view to another:   

<p align="center">
    <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/passdata.gif?raw=true"/>
</p>  

_I also added a "< Back" button. The concept of passing from one view to the other is the same. In this case, clicking the back button will move from the second view to the first view._

## Steps of setting up multiple views  
Last week, I jot down my steps of setting up multiple view in which resulted in an error. Below is the steps I took that has helped me avoid the errors i ended up with.  

1. Have the first view (View Controller) Setup  
    - Connect all components of the first view to view controller (by dragging)
2. Create a second view 
    - Create a new file > select Cocoa Touch Class > Give the class a name > subclass of UIViewController > next  
3. Go to the library and place a View Controller on the storyboard
4. Click on this new view and go the identity inspector
5. Set the class name of this second view to the name that you have assigned to the new file
5. Drag the button(or any other attribute you made) from the first view to the second view and click “show”
6. The connection is now being set up from the first view to the second view!

## App with multiple views
Now that I have learned how to set up views, pass on data, and many small parts I have tinkered throughout the past weeks, I was able to combine some of the projects I have already built into the following.   
    <p align="center">
        <img src = "https://github.com/xiurongy3506/swift_independent_study/blob/master/img/appsetup.gif?raw=true"/>
    </p>    

**Note**: The app is NOT complete. 

## What's next?  
1. The timer is yet to become a Pomodoro Timer
    - I will have to make the timer into user input
    - I will continue to research and think about how to make the user stay away from the screen when the timer is set
2. The user database (name, password) is yet to be set up
    - JL will set up MySQL database on my computer on Monday
    - I will learn how to set up OhMySQL Cocoapod starting Tuesday 
3. Passing on message data between two device
    - JL will create a message database
    - I will learn how to use Swift to send on messages

## Takeaways  
1. **Know your mistakes.** It is okay to fail at something, but it is not okay to not know where you fail and why you fail. For me, I was able to debug and fix my error from last week, and this takes time. However, while John was able to modify my code in a new file and fix my errors, I compared the solution code to the code I made to make sure I understand where my mistakes were at. Moreover, I write it down in this blog and how I fixed it. This process has allowed me to take in what I learn and use it again in the final app. 
2. **Know where you are at.** Knowing how much you have accomplished and how much you still have left to do can help you pace yourself. Understanding that there is a deadline to this project and what is still there for me to complete, I know that I will have to pace myself in a reasonable manner to make sure as much is done as possible.


