<!-- header which is bolded, bigger, and centered -->
<p align="center"><b><font size = 5>Essay 4</font></b></p>

<!-- Title of our essay -->
<p align="center">Appsmith's vs MIT App Inventor's Architecture Characteristics</p>

Introduction

Nowadays, we interact with apps on a daily basis. Since it's something so common, a lot of people may want to create an app of their own, however they may not have the requierd coding knowledge to create apps on tools such as AndroidStudio. Thankfully, there are open source projects available to help people with none to little coding experience to create the app of their dreams. First, there's [**Appsmith**](https://github.com/appsmithorg/appsmith), which we have been analyzing this semester, and another tool that is avaliable to develop apps is [**MIT App Inventor**](https://github.com/mit-cml/appinventor-sources). 

Even though the basic concept of these programs are similar, the audience for them are very different. MIT App Inventor is targeted towards people (mostly K-12) who want to get into coding and learn the basics. The interface of this IDE is similar to [Scratch](https://github.com/LLK/) where you can drag and drop blocks of code that connect with eachother. 

// Needs a little more work...

Appsmith Characteristics we studied:
- Modifiability
- Performance
- Configurability

How MIT App Inventor compares to Appsmith regarding modifiablity

// TODO

Performance
From the community discussion, we discovered that MIT App Inventor really struggles when it comes to trying to create larger applications through their app. This is obviously a trivial issue, but the issue never seemed to get fixed even though the community knows the driving problem. The problem occurs when too many blocks are on the screen at the same time. The number of blocks seems to be right around 5,500 and any more than that, the performance really trails off. Within the Github repo, they do not even have any issues related to performance which is very much so different from Appsmith where they took performance very seriously and had over 90 issues open that were directly related to performance. Within a discussion regarding MIT App Inventor's performance, one of the main contributors was quoted saying, "We don't have any concrete plans to work on the blocks editor performance at this time".


How MIT App Inventor compares to Appsmith regarding Configurability

Appsmith and AppInventor both implement configurability, but in different levels.
Appsmith provides hundreds of components that are all highly configurable. Appsmith allows you to configure size and placement of components, and edit the style and JavaScript code for each component.
AppInventor is also configurable, but not to the same extent as Appsmith. AppInventor also allows you to configure the size and placement of your components, but not styles or the JavaScript code.

An example is the map component. 
Appsmith allows you to change the border styles of the map, change size and placement on the app, connect to a database, add animations, enable various map settings, create markers, add onClick events, and more.
![image](https://user-images.githubusercontent.com/26784780/205799426-b63d786e-d296-4e6b-bace-0f5fd581e6e7.png)
![image](https://user-images.githubusercontent.com/26784780/205799539-eadf086c-971c-4768-afb6-a743d28b3a94.png)

Appinventor allows you to change the size and placement on the app, customize zoom/pan settings, add a compass, and road/terrian/arial map views.
![image](https://user-images.githubusercontent.com/26784780/205799762-e7f01b21-211b-4dd1-b5f7-04d252808598.png)

Both app creators are impressive, but there is a clear edge to Appsmith in terms of the level of configurability of their components.


Appsmith's codebase is additionally highly configurable, making it very easy for contributors to add additional widgets and tools. Appsmith's codebase makes this easy due to being incredibly organized, and with amazing code structure. No component exists that doesn't inherit from a base class.
Appsmith's codebase is organized in such a way that all of the backend portion of components are stored in the backend half of the repository, and all of the frontend components for the codebase is stored in the frontend half of it.
Within the frontend or backend side, each widget has every image, test, and additional files stored within that widget's frontend or backend file.
With this detailed organization, it is very easy to understand how to add new components, and what components will need to implement.

AppInventor's codebase is decently organized. They have folders containing their code for the frontend and the backend. However the insides of these two folders are not as easy to tell what in the backend connects to what frontend component. None of the backend components are named the same as the frontend components, so I was not able to identify what frontend components connect to which backend files. This is bad for configurability, since it makes it difficult to connect the dots, and to replicate it into future components.
For an example, recently there was a commit to AppInventor to add a "Delete Account" button. However to add this functionality, multiple files in multiple sources needed to be modified, and is not a characteristic of a highly configurable system.


What MIT App Inventor does well or poorly outside the three characteristics
Compared to Appsmith, MIT app inventor is much more lightweight and easier for a beginner to use. This leads to a very user-friendly interface that allows for apps to be created very fast and efficient. This is because MIT app inventor has drag-and-drop features that keep it simple and easy to use, but not as many as appsmith. While this keeps it simple, it also makes it more inefficient for large projects. Because of its simplicity, MIT app inventor excels at usability.
MIT App Inventor doens't do too poorly in documentation for developers, however it is very difficult to find anything about the structure of the app. They excel at documentation when it comes to setting up the environment, compiling it, and running the tests. MIT App invnetor also does well at keeping javadocs to document each individual component, however they have very little documentation about how components work together. Overall, these factors may end up causing newer developers to be unsure of how to go about solving an issue, having a negative impact on their maintainability.
Conclusion 
// TODO
