VendingMachine
==============

SMU Innovation Gym Vending Machine Software

This software is for the SMU Deason Innovation Gym Vending Machine. The software is built in python and runs on the Banana Pi, a dual core variant of the Raspberry Pi.

##Modules

###vendingMachine.py
vendingMachine.py is the main module.  It runs a wxPython GUI in a small window to present information to the user.  The workflow of the program is as follows:
  1. Prompt for swipe
  2. Read Swipe
  3. Check User balance/permissions
  4. If no permission: start over
  5. Else: Prompt item selection
  6. Check item balance vs. user balance
  7. If sufficient balance: Dispense item

Upon startup, the application loads the item list from the database using the dbAccess.py class.  The item list has the name of the item, the cost of the item, the quanitity of the item, and the physical slot number.

###dbAccess.py
dbAccess.py is the database interface class.  It provedes a number of functions for access and modification of database elements.  Some of the capabilities include:
  - Fetching the item list
  - Updating the item list
  - Fetching a user's balance
  - Updating a user's balance
In order to use the class, simply instantiate an instance of the class and call the proper function.

This module was written by Eric Johnson.

##To Do:
The software is largely operational, but lacks integration.  The following remains to be done:
  - Access Database for User authentication
  - Load items from database
  - Update item quantity in database after dispensing
  - Check user balance before dispensing
  - update user balance after dispensing
  - Mount hardware
  - Verify item was dispensed
