ATM System Project - C++

This is my ATM project for C++ course.
The program is like real ATM machine.

What the program do:
- Login with account number and pincode
- You can do Quick Withdraw, Normal Withdraw, Deposit, Check Balance
- After any operation the file Clients.txt will be updated

About Clients.txt file:
I save clients data in text file, each line is one client
and I separate by #//#
like: A111#//#12349329#//#Ahmad Zaid#//#079863212#//#44000

How the code works:

1- I made struct sClient to store client info (account, pin, name, phone, balance)
2- SplitString function to cut the line by #//#
3- ConvertLinetoRecord to change line to struct
4- ConvertRecordToLine to change struct to line again to save in file
5- LoadCleintsDataFromFile to read all clients from file to vector
6- SaveCleintsDataToFile to save vector to file
7- FindClientByAccountNumberAndPinCode to check login, loop on vector and check account and pin
8- CurrentClient is global variable to keep the client who logged in
9- For withdraw and deposit I use same function DepositBalanceToClientByAccountNumber, if amount negative it is withdraw, if positive it is deposit

To run the project:
Put Clients.txt in x64/Debug folder and run
You can test with A111 / 12349329

I used vector, fstream, struct, enum in this project.
