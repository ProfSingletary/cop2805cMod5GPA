# cop2805cMod5GPA

Welcome to Project Dandelo. This project requires you to design a command line-based
(no GUI) Java client/server application which transports kittens over the network
and stores them on a kitten server. The kitten client should prompt the user for
Kitten attributes (name, color, age, weight, litter box training status -- same
as the Kitten from the Module 2 ungraded practice exercise), create a Kitten object,
and send it to the server for storage.

The Kitten server should listen for connection requests and read Kitten objects into
a data structure which stores the objects. Only new objects should be added to storage,
if an existing object is received it should be checked for differences and the existing
one should be updated if differences exist, otherwise no storage operation is necessary.
Assume kitten names are unique for this assignment.

When an addition/modification occurs, the server should display the contents of storage
(show all of the kittens).

You should submit 3 files for this assignment: Kitten.java, KittenClient.java, and
KittenServer.java (or their equivalents).

Up to 5 extra credit points will be added for including, in the text submission area
of the assignment,  a sentence describing the historical significance of the name
"Dandelo" to this project. You must submit a non-trivial attempt at the programming
solution in order to earn these points.

Sample Output (client), user input shown annotated with "<==":

Welcome to the Project Dandelo client application.
Currently connected to the kitten server at address "localhost" on port 8000.
Please enter the name of a kitten: Snowball <==
Enter Snowball's color: white <==
Enter Snowball's age: 5 <==
Enter Snowball's weight: 3.5 <==
Is Snowball litter-trained? y <==
Snowball has been successfully transported to the server!
Please enter the name of a kitten: Mr. Snuffles <==
Enter Mr. Snuffles's color: grey <==
Enter Mr. Snuffles's age: 2 <==
Enter Mr. Snuffles's weight: 7 <==
Is Mr. Snuffles litter-trained? y <==
Mr. Snuffles has been successfully transported to the server!
Please enter the name of a kitten: Snowball <==
Enter Snowball's color: white <==
Enter Snowball's age: 5 <==
Enter Snowball's weight: 3.5 <==
Is Snowball litter-trained? y <==
Snowball has been successfully transported to the server!
Please enter the name of a kitten: Snowball <==
Enter Snowball's color: white <==
Enter Snowball's age: 1 <==
Enter Snowball's weight: 3.5 <==
Is Snowball litter-trained? n <==
Snowball has been successfully transported to the server!


Sample Output (server):

Welcome to the Project Dandelo server application.
Currently registered on port 8000.
New kitten received and stored: Snowball
Current kittens:
    Snowball, color=white, age=5, weight=3.5, litter-trained=y
New kitten received and stored: Mr.  Snuffles
Current kittens:
    Snowball, color=white, age=5, weight=3.5, litter-trained=y
    Mr. Snuffles, color=grey, age=2, weight=7.0, litter-trained=y 
Duplicate kitten received, not stored: Snowball
Kitten  received and modified: Snowball
    Snowball, color=white, age=1, weight=3.5, litter-trained=n
    Mr. Snuffles, color=grey, age=2, weight=7.0, litter-trained=y  