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

