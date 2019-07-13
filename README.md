# Groupus
It's a desktop application for the users to organize the events very well. Users could sign up, sign in, post events, search events and join events. 

The project is implemented under the git revision control and followed the basic rules for developing software. The whole design include the front end, back end, test parts, I undertake the back end part, which is implemented based on DAO design pattern.

Design user stories for above features firstly, the divide the backend code into three parts: database, data layer, and business layer. 

For database design, we select noSQL database Mongodb. Two collections have to be maintained in database for user information and event information respectively. 

Data layer design takes control of adding, updating, reading and deleting data from the database. We have to create an interface to uniform operating standards between data layer and database. In order to do this, we need to map the above two collections to be two value object classes. Besides, we need to build connections to database with the APIs provided by Mongodb instead of JDBC. In addition, factory class is used to return the object of the interface. 

For business layer, the goal is to implement the basic logic design according to user stories. An interface needs to be created between the business layer and control layer. This layer also wrapped CRUD operations mentioned above and provided it to the control layer. A factory class is used as well. Front end part is implemented by javafx framework. 

For the test part, we apply junit test for each method, use Jenkins server to do CI pipeline test and increase Increase both line coverage and branch coverage improved100% with enough test cases.
