<!-- header which is bolded, bigger, and centered -->
<p align="center"><b><font size = 5>Essay 4</font></b></p>

<!-- Title of our essay -->
# <p align="center">Appsmith vs. MIT App Inventor's Architecture Characteristics</p>

### Introduction

 Nowadays, we interact with apps daily. Since it's so common, many people may want to create an app of their own. However, they may need coding knowledge to create apps on tools such as AndroidStudio. Thankfully, open-source projects are available to help people with little coding experience create the app of their dreams. First, there's [**Appsmith**](https://github.com/appsmithorg/appsmith), which is the open-source project our group has been analyzing this semester. Then, there is [**MIT App Inventor**](https://github.com/mit-cml/appinventor-sources), which is another platform for developing apps. 

  Even though the basic premise of these apps is similar, their audiences are very different. MIT App Inventor targets students (mostly K-12) who want to start coding and learn the basics. The interface of the app's IDE is similar to [Scratch](https://github.com/LLK/). MIT App Inventor is a web app that allows users to create their UI with different components and attach events to these components in the Block Editor. Appsmith, on the other hand, is targeted toward businesses or large-scale software projects. Appsmith documentation has specific annotations and sections for the business version of their product.
  
  ![image](https://user-images.githubusercontent.com/26784780/205792540-c923b6fa-81b0-4b0c-934a-b6abf70887f7.png)

  Appsmith is a company that makes money off its product and has a large team dedicated to its success. Additionally, it is open source, allowing for community contribution, but the main contributors are full-time staff. AppInventor is a small nonprofit project from MIT and solely relies on open-source contributions for its code. With this, it makes sense that there will be large differences in the quality of code, architecture, and scale between the two projects.

## How does MIT App Inventor compare to Appsmith?
  The following sections will cover similarities and differences between Appsmith and MIT App Inventor's architectural characteristics of modifiability, performance, and configurability.

### Modifiability
  
  MIT App Inventor's codebase mostly uses the microkernel (plug-in) pattern. The web app comprises features that integrate and utilize different libraries and other projects, such as Google's Blockly and App Engine.
  
  For example, MIT App Inventor uses [Blockly](https://developers.google.com/blockly/) to let its users attach events and create functions in their [Block Editor](http://ai2.appinventor.mit.edu/reference/blocks/). MIT App Inventor's codebase has all the Block Editor functionality within a single module. This is advantageous for modifiability because all implementations and logic regarding blocks are grouped in a single module, which signifies increased cohesion. More importantly, a developer who desires to contribute to the app's Block Editor will only have to make changes inside its folder. This was evident when their team added a "join-with-separator block" in their app. This [pull request](https://github.com/mit-cml/appinventor-sources/commit/ceb27bf233d93e61ef741e9255149e1bb3e8ff8c) shows that almost all changes are inside the appinventor/blocklyeditor directory. However, App Inventor has coupling issues with its codebase as well. This [issue](https://github.com/mit-cml/appinventor-sources/issues/1997) explains the tight coupling between Project-related functionalities in their codebase, which was solved by refactoring to a closer "model-view-control separation of concerns."
  
  Appsmith also uses the microkernel (plug-in) pattern. As a project that should constantly evolve as the needs of its customers change, Appsmith needs to allow easy integration of new features. And, of course, Appsmith does a good job in this area. Developers who contribute to the app and use it can easily request/add new plug-in features in the open-source project. There are even [guidelines](https://github.com/appsmithorg/appsmith/blob/release/contributions/ServerCodeContributionsGuidelines/PluginCodeContributionsGuidelines.md) on how to contribute to the plug-in code. These detailed guidelines prove how well-structured is Appsmith's plug-in software pattern. 

  Overall, both projects effectively utilize the microkernel pattern to improve the modifiability of their codebase. The projects mostly differ in their module structures. Appsmith's codebase and customers are larger and more business-oriented than MIT App Inventor, so Appsmith will naturally want their architecture to be as good as possible—exhibiting loose coupling and high cohesion. Appsmith also has a larger contributors population. But still, MIT App Inventor has some good points with its modular architecture.

### Performance
  
  From the community discussion, we discovered that users find it difficult to create larger applications in MIT App Inventor. Even though the community knows the driving problem, the performance issue never seems to get fixed. The problem occurs when too many blocks are on the screen simultaneously. If the number of blocks is around 5,500, then the performance trails off any more than that. Within the GitHub repo, App Inventor does not even have any issues related to performance. This differs from Appsmith, which took performance very seriously and had over 90 issues directly related to performance. 
  
  Within a discussion regarding MIT App Inventor's performance, one of the main contributors was quoted saying, "We don't have any concrete plans to work on the blocks editor performance at this time" [**Discussion Link**](https://community.appinventor.mit.edu/t/performance-on-big-number-of-blocks-project/4995/12). This is reasonable because MIT App Inventor is targeted more toward education and learning, whereas Appsmith is toward more serious projects.
  
  There was only one other mention of performance issues anywhere within App Inventor's GitHub and discussion forum. This issue occurred when installing a developed application, and the TimerAlwaysFires was set to false. When TimerAlwaysFires is set to true, it constantly tries creating new screens, which leads the app to say, "application has stopped," and then, "this application reduces the performance of your device."

### Configurability
 
 Appsmith and App Inventor both implement configurability but at different levels. Appsmith provides hundreds of components that are all highly configurable. Appsmith allows you to configure the size and placement of components and edit their style and JavaScript code.
  
  App Inventor is also configurable, but not to the same extent as Appsmith. App Inventor also allows you to configure the size and placement of your components, but not styles or JavaScript code.

  An example is the map component. Appsmith allows you to change the map's border styles, size, and placement on the app, connect to a database, add animations, enable various map settings, create markers, add onClick events, and more.

![image](https://user-images.githubusercontent.com/26784780/205799426-b63d786e-d296-4e6b-bace-0f5fd581e6e7.png)

![image](https://user-images.githubusercontent.com/26784780/205799539-eadf086c-971c-4768-afb6-a743d28b3a94.png)

App Inventor allows you to change the size and placement of the app, customize zoom/pan settings, add the compass, and road/terrain/aerial map views.

![image](https://user-images.githubusercontent.com/26784780/205799762-e7f01b21-211b-4dd1-b5f7-04d252808598.png)

Both app creators are impressive, but there is a clear edge to Appsmith in terms of the level of configurability of their components. 

In terms of code organization, Appsmith's codebase is highly configurable, making it easy for contributors to add additional widgets and tools. Their codebase is separated into the client and server folders. Within the client or server side, each widget has every image, test, and additional files stored within that widget's frontend or backend file. This detailed organization makes it easy to understand how to add new components and what components still need implementation.

Meanwhile, App Inventor's codebase is decently organized. They have folders containing their code separated by functionality. However, when going through these folders individually, it becomes difficult to differentiate which components are implemented in the frontend or backend. None of the backend components are named the same as the frontend components, so it was hard to identify which frontend components connect to which backend files. Another example of this difficulty is exemplified in a commit to the App Inventor repository to add a "Delete Account" button. However, to add this functionality, multiple files in multiple sources had to be modified, which is not a characteristic of a highly configurable system.

## What MIT App Inventor does well or poorly outside the three characteristics?

Compared to Appsmith, MIT App Inventor is much more lightweight and easier for a beginner. This leads to a user-friendly interface that allows apps to be created quickly and efficiently. This is because the MIT App Inventor has drag-and-drop features that keep it simple and easy to use, but not as many as appsmith. While this keeps it simple, it is also more inefficient for large projects. Because of its simplicity, the MIT App Inventor excels at usability.

MIT App Inventor doesn't do too poorly in the documentation for developers. However, finding something about the app's structure takes a lot of work. They excel at documentation regarding setting up the environment, compiling it, and running the tests. MIT App Inventor also does well at keeping Javadocs to document each component. However, they need more documentation about how components work together. Overall, these factors may cause newer developers to be unsure of how to solve an issue, negatively impacting their maintainability.

## Conclusion 

Ultimately, MIT App Inventor is less adaptable, performance-driven, and configurable than Appsmith. However, MIT App Inventor does not need to be as well-structured as Appsmith because these projects have different target users with different needs. Overall, MIT App Inventor thrives as a smaller-sized app, satisfying its goal of educating the youth ["to move from technology consumption to technology creation."](https://appinventor.mit.edu/about-us)
