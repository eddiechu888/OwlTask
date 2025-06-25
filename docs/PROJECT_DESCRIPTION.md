Final Project Description
This description and its requirements are subject to change, so please always refer to the latest version of this page!

OwlTask
Each student project group will design and implement their own version of the OwlTask application.  The general description and requirements described below are deliberately vague to allow each group a measure of customization of the application to match their conceptualization of the application and what it is able to accomplish for the user.

Description:
The primary focus of OwlTask is to enable the

Creation of tasks that assigned across individual or groups of users
Management and coordination of those tasks.  
The system should be highly flexible and allow real-time management, coordination and monitoring.  The system should be inherently flexible and extensible to handle a wide range of situations both now and in the future.

That said, in a typical application, probably more than 75% of the implementation code has nothing to do with the directly stated purpose of the application.  Most of the implementation goes towards supporting the infrastructure of the application and not the user "features" directly. Looking past the outward purposes for the user, what is most of this application really about?  What comprises the majority of most applications' implementations?

 

Non-Exhaustive List of Possible Features and Capabilities
Here is a list of possible features and capabilities to help you get started on thinking about what this app is really all about.   This is far from a complete list -- assume everything has an "etc." at the end!

An application is NOT just a collection of features!  The job of any feature is to help deliver the fundamental goals of the application.

Concentrate on understanding the key jobs that the application is doing for the user and then choose the highest priority features that enable it to accomplish those tasks.  And thus, there is also no minimum number of expected features.

"The tool changes the way that you see the job."  Always assume that the list of features and capabilities WILL increase and/or change over the lifetime of the app!  

Users
Types of users  ("audiences" or "persona")
General users -- People who are using the app to accomplish the goals of the app.
Application administrators -- People who are in charge with managing the app's operation, e.g.  user management, component upgrading, monitoring, etc.
System maintainer/developers -- People who are responsible for maintaining the application's software such as updating the core system software, bug fixes, new feature development, etc.
Groups of users
Group roles, e.g. leader, documentation manager, etc.
Groups of groups of users allowed 
Single-line vs. multi-line hierarchies.
Authentication (verification of identity)
Federated authentication:  Not handled by the app, e.g., via Google or ADRICE (NetID) login.
Authorization (allowed permissions)
Individual permissions
Group permissions
"Whitelisting" vs. "blacklisting" vs. combination --
Allowed if specified but denied if not specified ("whitelisting"), or
Denied if specified but allowed if not specified ("blacklisting") or
Allowed or denied if specified but denied otherwise -- Not the same as the other choices with respect to automatically overridden permissions due to inherited permissions, e.g. can explicitly deny access to a group of users even if some individuals in the group would normally have access.
Hierarchical permissions
Inherited permissions via a group hierarchy.
Multiple inheritance from multiple groups can be problematic.
Automatically overridden permissions -- To handle permissions conflicts.   
Management 
Authorized users and groups
Adding/removing new users and groups
Managing permissions of individuals and groups.
Tasks
Aspects:
Description
Categorization -- e.g., area, sprint/milestone, etc.
Hierarchal categories
Priority
Due date
Restrictions on who can be assigned -- e.g., location, roles, permissions
Projected resources needed
Current status
Assignable to:
Individual
Group 
Composite tasks -- tasks with sub-tasks
composee-task restrictions due to composite task settings --  e.g. composee task must be assigned to member of composite task assigned group.
Managment:
Task updating -- properties, deletion, etc.
Real-time status monitoring
Filtered display based on groups, categories, etc.
Alerts
Changes
Overdue
Communications
Chatting/discussion on task issues
Individual or group discussions
Real time updating for connected users
Notifications upon connection for disconnected users.
Archived and searchable
Notifications.
In real-time to connected users
Upon connection for disconnected users.
Scalability
System should be inherently scalable to handle large numbers of users, groups and tasks.
Responsive User Interface
Usable from a variety of devices, e.g., desktop, tablet or phone in portrait or landscape modes.
 

It will NOT be possible to implement all possible features!  But any omitted features MUST be discussed in terms of the rationales as to why they were omitted with respect to those features that were included and what sorts of development efforts would be required to add them later.

 

Implementation Requirements
While there are many, many ways to implement any application, for the purposes of this course, the following implementation requirements are imposed:

The application must be a web application using an MVVM architecture and it must be deployed on Heroku.
Note that the starter code already contains the heroku.yml and Dockerfile needed to deploy both the Java and Next.js systems to Heroku as a Docker container.
The application must use good design principles throughout with explicit use of design patterns to solve appropriate issues.
A minimum of four of the software design patterns covered by the class should be employed.
The application front end (browser side) code must use JavaScript or Javascript-based language (e.g. React, Angular, TypeScript, Redux, etc.) 
The network communications must utilize a bi-directional, asynchronous message-passing API for communications between the clients and server using a web socket.
The server should be written in Java and use Spark Java to implement the web socket.
System should be inherently scalable to handle large numbers of users, groups and tasks.
Internal system architecture should be easily refactorable to enable greater scalability and/or performance, e.g. employ well-encapsulated operational task implementations that could easily be separated into independently scalable sub-applications/functionals.
User interface should employ "responsive" display techniques that enable the application to be usable from a variety of devices, e.g., desktop, tablet or phone in portrait or landscape modes. 
If there are alternative implementation techniques that you feel are in line with the goals of the course but potentially disallowed by the above requirements, please bring them up during class and/or make a public Piazza post to discuss the issue.  If an alternative is acceptable, the project description will be amended to include it.

Being a capstone-level project, it is highly recommended that the application involve an in-depth exploration of at least one or more of the major Computer Science topics you have studied in other classes in the MCS@Rice program (Machine Learning, Databases, Data Visualization, Systems Software, Big Data, Algorithms, Programming Languages, Statistics or Cyber Security).

 

Allowed Restrictions:
In light of the limited time frame to complete the project, the following restrictions will be allowed:

Browser-based application only:  Access to application is only through a web browser and notifications need only be alert messages in the browser.
Single server instance only:  While the architecture should express an inherent scalability, only a single server instance deployment is required.
 

Project Deliverables
Each Final Project team will deliver a single implementation of the application.    Unless otherwise specified, the scores assigned to the various deliverables will be a group-score.   See the linked assignments for more details.

Software Requirements Specification
Requirements Document (Individual) -- Individual notions of application specifications to be used to create the specifications of the delivered application.
Group: Finalized specifications of the delivered application.   Part of the project plan and final documentation below.
Project Plan (Team)  
Architecture Document (Team)
Use Case and System Block Diagram (Team)
Database Design (Team)
Design Document (Team) 
Test Plan (Team)
Presentation (Team)  -- includes demo
Final Project Report (Team) -- Final documentation
 

 

Advice
KEEP IT SIMPLE!!

It is much better to deliver a fully operational application with fewer features than a broken application with lots of features.

 

DOCUMENTATION DRIVES DEVELOPMENT

If it's not written down, it doesn't exist!    Project documentation is to communicate what WILL be done, not what was done.  Final, delivered documentation is just a recap of the on-going project documentation.

Good documentation is what holds the team together.

 

IDENTIFY AND FOCUS ON THE CORE CAPABILITIES OF THE SYSTEM.   

An application that cannot deliver its core capabilities to the user is useless to them.   

Make sure that the system architecture is fundamentally able to grow and evolve with the ever-changing needs of the users and the application itself.

EXTENSIBILITY IS MUCH MORE IMPORTANT THAN FEATURE COUNT!

You won't have time to add features that are just "cool" and "nice to have" -- but make it so that it is easy to extend the system to include them!

As stated above, remember that most of the application's implementation will not be explicitly tied to the outward purposes of the app for the user.   Look beyond the specifics of this application to find what most of this application is really doing.    Many of the "features" are just examples of a much more general operations.    

 

RISK ANALYSIS DRIVES DEVELOPMENT PRIORITY

Everything done as part of the development process has some level of "risk" because there is always a non-zero probability of failure and a resultant impact on the application and/or its development.    The higher the risk, the higher the development priority. 

Plan EARLY and COMPLETELY!   The #1 problem in risk planning is insufficient detail (e.g. lack of completeness and/or vagueness).

 

ASK EARLY AND OFTEN!

You don't have time to pound your head against the wall!

Make public Teams posts (i.e. not private chats or emails) as this will both tap into the larger experiences and viewpoints of others and benefit everyone in the class!

Upon request, technology resource lists and pages can be created to facilitate the development process.   This course is not about becoming technology experts but rather on learning how technology can be used to implement good design.

 

Tips and Traps
See the Final Project Resources and CS-SOFTENGR - Home Links to an external site. sites!
Lots of links and pages covering everything from design concepts and techniques, technologies, Heroku and GitHub deployments, and much, much more!

 

Synchronizing the JSON data types between the frontend and backend
The starter code already includes the typescript-generator tool that can automatically update the TypeScript definitions of data types defined on the Java side of the system.   This is very useful for ensuring that the frontend and backend definitions for the JSON data types are consistent.

For more complete information, including usage instructions, please see CS-SOFTENGR - Java-TypeScript Generator Links to an external site..

IMPORTANT:   The pom.xml file may need to be modified slightly to accommodate your project's specific needs. 

As configured from the assignment starter code:

JSON message data packages (<classsPatterns> tag -- note that each package must be specified individually!):
 ballworld.viewModel.msgs
ballworld.viewModel.msgs.jsonDataTypes
Output TypeScript file (<outputFile> tag):
src/app/jsonDataTypes/types.ts
 

