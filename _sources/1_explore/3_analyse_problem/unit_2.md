# Unit 2: Analyse the Problem
How you display databases in Use Case Diagrams depends on the type of database you are using.

Effectively (for Use Case Diagrams) there are two types of databases:
- **internal database:**
  - characteristics:
    - created and maintained by the code of your propgram
    - resides on the local machine your program is running on
    - each copy of your program will access its own seperate database
  - Use Case Diagram representation:
    - **not** considered an actor for Use Case Diagram purposes
    - included within the system box of the diagram
- **external databases:**
  - characteristics:
    - created and maintained by code which is sperate from your program
    - resides on a server seperate from the local machine
    - each copy of your program will access the one database via the server
  - Use Case Diagram representation:
    - considered an actor for Use Case Diagram purposes
    - drawn as a secondary actor to the right of the system box