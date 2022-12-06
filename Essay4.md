<!-- header which is bolded, bigger, and centered -->
<p align="center"><b><font size = 5>Essay 4</font></b></p>

<!-- Title of our essay -->
<p align="center">Appsmith's vs MIT App Inventor's Architecture Characteristics</p>

Introduction

Nowadays, we interact with apps on a daily basis. Since it's something so common, a lot of people may want to create an app of their own, however they may not have the required coding knowledge to create apps on tools such as AndroidStudio. Thankfully, there are open source projects available to help people with none to little coding experience to create the app of their dreams. First, there's [**Appsmith**](https://github.com/appsmithorg/appsmith), which we have been analyzing this semester, and another tool that is avaliable to develop apps is [**MIT App Inventor**](https://github.com/mit-cml/appinventor-sources). 

Even though the basic concept of these programs are similar, the audience for them are very different. MIT App Inventor is targeted towards people (mostly K-12) who want to get into coding and learn the basics. The interface of this IDE is similar to [Scratch](https://github.com/LLK/) where you can drag and drop blocks of code that connect with eachother. 

// Needs a little more work...

Appsmith Characteristics we studied:
- Modifiability
- Performance
- Configurability

How MIT App Inventor compares to Appsmith regarding modifiablity

// TODO

Performance
From the community discussion, we discovered that MIT App Inventor really struggles when it comes to trying to create larger applications through their app. This is obviously a trivial issue, but the issue never seemed to get fixed even though the community knows the driving problem. The problem occurs when too many blocks are on the screen at the same time. The number of blocks seems to be right around 5,500 and any more than that, the performance really trails off. Within the Github repo, they do not even have any issues related to performance which is very much so different from Appsmith where they took performance very seriously and had over 90 issues open that were directly related to performance. Within a discussion regarding MIT App Inventor's performance, one of the main contributors was quoted saying, "We don't have any concrete plans to work on the blocks editor performance at this time" [**Discussion Link**](https://community.appinventor.mit.edu/t/performance-on-big-number-of-blocks-project/4995/12). This seems reasonable because MIT App Inventor seems to be targeted more towards education and learning whereas Appsmith is more directed towards more serious projects. There was only one other mention of performance issues anywhere within the Github and the discussion forum. This other issue occured when installing a created application and not having TimerAlwaysFires set to false. When TimerAlwaysFires is set to true, it constantly tries creating new screens which leads the app to saying, "application has stopped" then, "this application reduces the performance of your device". 


How MIT App Inventor compares to Appsmith regarding Configurability

// TODO


What MIT App Inventor does well or poorly outside the three characteristics

// TODO

Conclusion 
Ultimately, MIT App Inventor is not as performance driven as Appsmith, but does not really need to be as it thrives in smaller sized projects. 
