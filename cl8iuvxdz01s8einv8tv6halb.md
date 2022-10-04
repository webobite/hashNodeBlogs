## Micro frontend in UI Development

> Disclaimer: This blog is for the reader who has some amount of understanding as well as has worked on some large projects dealing with scalable application objectives as a major chunk of their work.

Working on medium to large-size software projects with multiple development teams architects and software development teams face problems. The problems are common **communication between the development teams** and **interdependence between the members of different teams for their respective work**. These problems result in delays in software development, and conflict in coding standards during the development process as different teams follow their respective coding standard at their convenience.

**Micro frontend** architecture was introduced in UI development to address this problem. Here different teams can work on the same projects following their own coding practices and standards. Hence, reducing the dependency and conflict in codes with other respective teams, and making the software development process fast and independent of other teams. 

> In simple words, micro frontend is an architecture where the UI components are developed, build, and deploy independently, rather than coding all the UI components in the main project. In the main project, all these UI components which are deployed separately are added as project dependencies to create a software system as a whole.

Ok... let's deep dive to understand more about it.

## UI Architecture for Micro frontend  

Here in this type of UI architecture, we mostly have two types of code repositories to 
develop and maintain : 

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664199033581/s6S2Jfcl7.png align="left")

### Main Project repository 
In this project, all independent UI components (widgets) are built and deployed on the server are added as dependencies, and consumed in the View layer of the UI application.

### Separate UI components (micro frontend app) 
- These are separate UI component projects (widgets/features) that are built and deployed as a separate dependency for the main project. 

- Each of these UI component repositories is owned by different teams in the organization which helps to reduce dependency among different teams and hence reduces code conflict and makes development faster. 

- Here each team works on a common project, which owns a separate feature in the project instead of working on the same code base in the main app. Once the development is done, the feature is integrated into the main app by the respective team itself.

> Ok... So until here hope you are getting the point... Now A question arises What about the communication between the different components which are integrated into the main app?

## Communication between separately Integrated UI components in the main project
For communication independently developed UI components, in the main project following ways are used in the UI framework : 

- ### Custom Events using browser API
It is one of the ways to communicate between the components, which also helps indirect coupling between the two or more independent components.

- ### Using the model of properties in the UI components
This model is mostly for frameworks like React which uses a properties model to pass on the data from one component to another, helping in maintaining the loose couple between the Independent component in the main application. 

- ### Via routing to pass on the data from one component to another component screens. 
Pass the data through the routing URL between different screens. It is also one of the prevalent approaches to be followed in the micro frontend to share data among themselves.

## When to choose or switch to micro frontend architecture for UI Development? 
It’s not compulsory to implement a micro frontend in every UI project that the team is working on in an organization. It is a matter of call depending on the circumstances that the project requires to be addressed or whether the team is facing any issues that can be resolved with micro frontend architecture.  
Here are **some common issues which can be addressed with the micro frontend**: 

1. When project size is mostly of medium to large size consisting of lots of complex features which can be subdivided into different UI components. 
2. When there exist multiple teams working on a single project. 
3. Codebase size has become difficult to maintain and manage.

> It depends on the call of the architect and team members of that project responsible to decide on the same

## Downsides of using micro frontend in UI development 
Implementing a micro frontend in UI also comes with some downside, which also 
needed to be taken into mind. 
Here are a few listed downsides for the same :

1. ### Increase in payload size 
      Independently deployed bundles can cause code duplication of common dependencies and increase build payload size, so every time the end-user opens the web application needs to download the micro-frontend build for getting render the UI 

    However, there exist some ways to resolve this part with segregation of the common dependencies during the final production build but they are also not the full-proof way to remove this downside. 

    Impact the page performance in rendering the UI for that project because of the large build size. 
2. ### Operational and cost increase
    As discussed, for implementing the micro frontend one needs to add multiple deployable code servers and maintain that respective code and server too, which adds to the cost for that project development and even maintaining the same. 

## Testing 
Testing in the micro frontend is similar to what the team test the monolithic application. Here, each team tests its application on different levels. The test is usually comprised of : 
- **unit testing** which is used to test most modular parts of the micro frontend app. 

- **Integration testing** is used to test the integrated part of different modules in that 
micro frontend. 

- **browser-based-end-to-end tests** is the testing commonly on the browser side 
with automated scripts to test the end-to-end functionality of the app. 

In micro frontend projects, end-to-end testing/browser-based UI testing can be 
categorized in two parts : 
- **Isolation**: In an isolated environment (sandboxed) team perform a large part of 
their user interface test without the code of any other team. Here mostly the test 
are run with mocked data. 
- **Full Integration**: For the critical transition points in the full integration of 
application a full integration test is added to trace the possibility of errors in the user 
interface boundaries too.

## Conclusion 
As discussed micro frontend is a matter of call and not a compulsory tool for UI development, it needed to be chosen very wisely as the has some downsides too. Applications in today’s industry are more focused on being scalable and more maintainable systems. A certain boundary needed to be defined to maintain a balance between coupling and cohesion to deliver the scalable product. 

> In the next blog will try to come up with some code implementation for the Microfrontend concept.

Stay Connected by Following me over @[Subham Singh](@webobite)

Thanks For your time Do comment your feedback

Stay safe and Healthy 😊 <br/>

Thanks & Regards<br/>
Subham


