
Red Carpet Up 
GST Tax System Assignment


		Applicant Name: Atriya Patel
		Language: Python (3.9) Flask Framework
		Contant: 8141197449, atriya.patel@gmail.com



Proposed Design

1.	There are 3 Tables [ User, Tax-Payer, Tax]
2.	When account is made it is by default a Tax Payer
3.	Later Admin can change the role of User to Accountant 
4.	We never allow accountant to create account we only change it by Admin. This way only Admin can make new Admin or Accountant.
5.	The Admin URL is secured by Basic Auth known by Admin only.
6.	Rest end points are secured by Login system.
7.	Simple UI of Flask is provided for Tests and admin.

Note: Primary focus is Security and System Design. UI can be easily modelled according to exceptions for error handling (Like incorrect date format, blank password etc.) It can throw error but backend is secured to not let it Pass.


Test Cases

1.	Creating a Tax-Payer Account

A.	Start Flask Server and Go to Home Page Create an Account with Email & Pass.
B.	A Tax Payer must register his Business. A Tax Payer can have only 1 Business.
C.	Now after business is registered it will show a welcome message with Business name and Tax dues (If not any dues, then No tax Dues message)

2.	Creating an Tax Accountant’s Account 

A.	As discussed Earlier only admin can change the role of user.
B.	Hence, we make other simple User Account Again but DO NOT Register Business. Just close the tab
C.	Now we go to Server-address / admin like (http://192.168.0.106:5000/admin/) URL Just like Django.
D.	 Now as we are entering as Admin, we will be asked Username & Password We can use a strong Credential but for simplicity of testing 
				Username: root 
				Password: root
E.	Now in Admin Panel we go to User Table and change role of Account we created to Accountant from Tax-Payer

3.	Issuing Tax Due and Editing Data of Tax Payer

A.	Log in with Accountant Account from Home page.
B.	You will see Data of all Registered Businesses with Edit button feel free to try.
C.	All issued Taxes will be also shown with Edit button.

D.	Now to on top just after welcome message in a text box Enter GST Number of any Registered business and Click on Create a Tax Due.
E.	Now Feel the details asked in the form just like we do in GST challan (https://payment.gst.gov.in/payment/createchallan).
F.	Isse the Tax Due



4.	Checking the tax due in Tax Payer Account 

A.	Open the Tax payer account to we just issued a tax due 
B.	Now you will see a tax due with Pay button at bottom. 
C.	On clicking Pay, If due date is not passed then only it will be deleted and success repose will be shown.
D.	If due date is already passed then we will see a message saying cannot Pay tax now.


Demo Accounts (Already Present in DB)

1.	Tax Payer Account  

	Email:  john@gmail.com
	Pass:  123

2.	Accountant Account 

	Email: mat@gmail.com
	Pass:  1230

3.	Admin URL Auth Details 
		Username:  root
		Pass:  	 root 





