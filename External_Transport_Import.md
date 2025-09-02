-<!--Author: Aman Kumar-->
<!--Date: 02-09-2025-->
<!--This markdown file details the procedure to import an external package to an SAP system.-->
## :inbox_tray: How to import an External Transport Request into an SAP system?

#### Step 1 : Download the data and co-file from the source system's transport directory onto your local PC using the following TCode:
```
/ncg3y
```
#### Step 2 : Upload the data and co-file onto the target system's transport directory using the following TCode:
```
/ncg3z
```
#### Step 3 : Add the external TR to the target system's import queue / buffer. Extras->Other Requests->Add.
![](https://github.com/amancs1422/Practice_SAP/blob/2084506c92ebff8b49c8ff4963e662efd03f45ea/Images/External_TR1.jpeg)
#### Step 4 : Fill in the transport request number, target client and click on continue.
![](https://github.com/amancs1422/Practice_SAP/blob/2084506c92ebff8b49c8ff4963e662efd03f45ea/Images/External_TR2.jpeg)
#### Step 5 : Follow the usual import procedure going forward.

-AK