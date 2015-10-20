# GitReporsitory

What is it?
 This document is about RouteOne Code Test, written in java and 


packaged as executable jar file as purchaseoder-0.0.1-SNAPSHOT.jar

System Requirement:

It has been built in JDK 1.8 in Mac OS X machine. Also, it has been tested in JDK 1.6 in Windows machine. Executable jar contain all the dependency library files so, it doesn’t required any external runtime lib reference.

Assumption:

When running Purchase Order program with no input argument, supplied static input parameters to get default purchase list. This is just to give an idea what it does when you run with no parameters.

Inventory List that is being used: PC1033 20 RAM PC800 9.99 RAM GenericProcessor 1100 CPU GenericMotherboard 105 MB GenericMotherboardV2 100 MB LCD 9.99 PERIPHERAL Keyboard 15 MISC GC800 9.99 RAM

Input: List of items to be purchased (Supplied by runtime argument) Output: 1) Valid purchase item in sorted order. 2) Total price of the purchase in a formatted to local currency Ex. $1,000.00

How to execute: 

Ex1 - Execute jar file with NO passing arguments


java -jar purchaseoder-0.0.1-SNAPSHOT.jar —> Default purchase order will appear as below if don’t supply runtime argument

GenericProcessor,PC1033,Keyboard,GC800,LCD,PC800 - List of purchase items Purchase Total: $1,164.97 - Total amount on valid purchased items.

Purchased items would appear as sorted on price (Higher to lower), if two items with same price, those items will be sorted again on alphabetical order.

Ex. per above result, GenericProcessor has highest price and Keyboard is higher than PC800, LCD and GC800, since PC800, LCD and GC800 all have same price 9.99, these three of items sorted on alphabetical ascending order as it appear above.

Ex2 - Executing with Runtime argument


java -jar purchaseorder-0.0.1-SNAPSHOT.jar GenericMotherboard PC800 PC1033 ABCD Out of Inventory: ABCD

GenericMotherboard,PC1033,PC800 Purchase Total: $134.99

In 2nd execution, suppled runtime arguments as purchase list as above. If the item is not available in inventory, which will be considered as ‘Invalid’(Out of inventory) as appears for the item “ABCD”. We get the itemized list for rest of the valid items in the above said order.

Also, You may see logging events get logged into purchaseorder.log in current directory where the program gets executed.

Thanks,
Krishnan
