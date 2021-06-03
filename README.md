# group45-ICG
ICG group assignment
Customer_SignUP_Page 
START
VARCHAR name
VARCHAR email
NUMBER age 
NUMBER payment
CHARACTER address 
CHARACTER password

INPUT “Enter your age”
STORE INPUT IN age 
INPUT "Enter your name and surname"
STORE INPUT IN name 
INPUT “Enter your email”
STORE INPUT IN email 
INPUT “Enter your payment details”
STORE INPUT IN payment 
INPUT “Create password”
STORE INPUT IN password

IF age<16 THEN 
    OUTPUT “You cant create an account”
ELSE 
  OUPUT “welcome”+name
ENDIF
END

Customer_Login

START 
INPUT “Enter your email”
Get email 
INPUT “Enter your password”
Get password 
If email and password valid THEN 
ENABLE Login
ELSE
Error message “Password or email invalid”
ENDIF
END 

Employee_SignIn
START 
INPUT “Enter your ID”
Get ID
INPUT “Enter your password”
Get password 
If ID and password valid THEN 
ENABLE Login
ELSE
Error message “Password or ID invalid”
ENDIF
END 


Calendar_Dates
START
Birthday_Discount = 50% off
anniversary_Discount = 25% off
Christmas_Day = 50% off 
PROMPT Customer for Important Calendar dates 
GET customer birth_Day 
STORE on Calendar_Dates as BirthDate
PROMPT Customer if MARRIED or SINGLE OR OTHER 
IF MARRIED 
STORE on Calendar_Dates as anniversaryDay
IF calendar_Date matches BirthdayDate
DISPLAY “you get 50% off”
  ELSE IF Calendar_Dates matches anniversaryDay
    DISPLAY “A you tied the knot today , you get 25% off ”
 ENDIF
END 


Customer_Care 

START 
       PROMPT user if user needs assistance 
       DISPLAY “YES” or “NO” options 
         IF “YES” 
          DISPLAY “ You are being transferred to an agent”
            ELSE IF “NO” 
               DISPLAY “In that case have fun shopping! Remember to click on the help toolbar if you are in                                                                                             of need of assistance”
        ENDIF 
             END


Add_TO_Cart
 START 
INT nItem1,nItem2,nItem3,nItem4,nItem5
PROMPT user to add item to cart 
STORE users input 
IF user selects Proceed_TO_Checkout
      ADD item1+item2+item3+item4+item5 = TOTAL
        DISPLAY TOTAL
PROMPT user to confirm Payment details 
IF valid then display “ thank you for your purchase, your package will arrive in two business days”
    ELSE Display “ unable to confirm purchase”
ELSE IF user selects EXIT THEN 
      ENDIF 
END

 
Customer_Rating 

START

PROMPT if user has time to complete a quick survey

Display YES or NO options.

        IF NO

DISPLAY "Thank you for choosing us for your beuaty supply needs"

           ELSE IF YES

PROMPT user if they enjoyed their shopping experience

DISPLAY YES or NO options

              IF NO

Prompt if user has any concerns about services

Get user input

              ELSE IF YES

PROMPT user if any changes should be made to enhance experience
Get user input 

ENDIF
END 

Database for Customer-Company Relation (Done By Jose Clayton AND Marlven Bhunu Shava)
CREATE TABLE Customers
 (Customer_ID INT NOT NULL,
First_name CHAR(25),
Surname CHAR(50),
Age INT,
DOB DATETIME,
PRIMARY KEY(Customer_ID) );
Customer_ID	First_name	Surname	Age	DOB
2576829	Catherine	Van Vyk	27	14/09/1995
2647892	Stephen	Scheinder	40	08/02/1981



INSERT INTO Customer
(Customer_ID, First_name, Surname, Age, DOB,) VALUES
 (2576829, ‘Catherine, ‘Van Vyk’, 27, ‘14/09/1995’),
(2647892, ‘Stephen’, ‘Scheinder’, 40, ’08/02/1981’) );
 
 
CREATE TABLE Customer Contact Details
                   (Cellphone_no VARCHAR(15),
                   Telephone_no VARCHAR(10),
                   Email CHAR(25),
                   P.O.BOX INT,
                  FOREIGN KEY(Customer_ID) );        

Customer Contact Details
Cellphone_no	Telephone_no	Email	P.O.BOX	Customer_ID
081-657-0000	061-5477	CVanWyk@yahoo.com
14930	N2576829S
081-456-7656	061-3768	StephSch@yahoo.com	14782	N2647892S
INSERT INTO Customer Contact Details
 (Cellphone_no, Telephone, Email, P.O.BOX) VALUES
(081-657-0000, 061-5477, ‘CVanWyk@yahoo.com’, ‘P.O.BOX 25000’),
(081-456-7656, 061-3768, ‘StephSch@yahoo.com’, ‘P.O.BOX 24076’) );

 
CREATE TABLE Products
        (Product_no INT PRIMARY KEY,
        Product_name CHAR(80) 
       Product_type CHAR(50)
       Product_price FLOAT) );
Products
Product_no	Product_name	Product_type	Product_price
S039989Q	Atlanta Shampoo	Hair Product 	40.50
Q990038E	Everest Skin Moisturizer 	Cosmetics	68.90





INSERT INTO Products 
(Product_no, Product_name, Product_type, Product_price) VALUES
(039989, ‘Atlanta Shampoo’, ‘Hair Product’, 40.50),
(990038, ‘Everest Skin Moisturizer’, ‘Cosmetic’, 68.90 
CREATE TABLE Customer Section
         (Products_no INT
         Comments CHAR(100),
         Preferences CHAR(50),
         Anniversary_date DATE,
         DOB DATE,    
         FOREIGN KEY(CUSTOMER_ID) 
         REALTIONAL KEY (Products_no) );
Comment Section
Customer_ID	Product_no	Comments	Preferences
2576829	039989	Very good product. Takes the cup for me.	Should remain exactly as it is
2647892	990038	Poorly labelled and advertised. Far from satisfactory.	Would love it to have a greater smoothening effect.
INSERT INTO Customer Section
(Customer_ID, Products_no, Comments, Preferences,) VALUES
(2576829, 039989, ‘Very good product. Takes the cup for me’ ,’ Should remain exactly as it is’),
(2647892, 990038, ‘Poorly labelled and advertised. Far from satisfactory’, ‘Would love it to have a greater smoothening effect’)


 
Table for Employee Management 
CREATE TABLE Employee
     (Employee_ID INT NO¬¬T NULL	
      First_name CHAR(50)
      SURNAME CHAR(50)
      Department CHAR(50)
      Postion CHAR(50)
      Attendance CHAR(15)
Employee
Employee_ID	Frist_name	Surname	Department	Position
7689076	Maxine	Phoeman	Sales and Marketing 	Head Sales Clerk
3456754	Sydney 	Matheaus	Research and Testing 	Senior Lab Researcher 
INSERT INTO Emloyee
(Employee_ID,First_name,Surname,Department,Position,) VALUES
(7689076, ’Maxine’, ’Phoeman’, ’Sales’, ’Head Sales Clerk’,)
(3456754, ’Sydney’, ’Matheaus’,’Research and Testing’ ,’Senior Lab Researcher’) );


Modules:
SignUp module: This module allows for a user to be able to create an account and set a password to it
Login Module: This module allows a user to login into their account by enteing their username and password, provided they have already completed the signUp module.
Login History: This module keeps track of the Login history. It can only be viewed by the admin. It provides employee and customer
login time and logout time. Through this the admin knows who frequently has been on the site.
Cart module: This module shows the items that have been added to the cart before the customer proceeds to checkout. It also shows an order summary and allows for the user to add or remove items from the list.
Gift card module: This module can be used on a checkout page to redeem a gift card as tender.
Payment module: This module lets customers pay for orders by using credit cards or debit cards.
Checkout module: This module captures the shipping address, shipping method and billing information. It is required to succesfully make an order.
Logout module: This module allows a user to safely signout of the page without them leaving their profile exposed to foreign entities.
Customers Account module: This modules keeps track of user orders and history so that Re-orders, user address, Product reviews and customer contact detatils are easily accesible to admin on site.
Catalog management module: This module allows to keep track of item quantities and provides specific information and characteristics of items in catalog, It also allows for easy search of items.









