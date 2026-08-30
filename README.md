# BUV Hotel Star Rating - Guest Feedback System
## A Python-based system for collecting and analyzing guest satisfaction
### 1. Overview
This Python project allows users to create and read feedbacks. Guests can rate different aspects of their hotel experience,
provides an overall satisfaction and feedback report 

### 2. Setup
**Requirements**
- Python 3.x
- User input
- Terminal
### 3. Operation
** Main menu **

- The program displays 4 options:
1.  **Give Feedback** 
2.  **View Feedback** 
3.  **Feedback Report** 
4.  **Exit** 
 Users choose an option to determine which function to run

**Give feedback**

- When the user choose 1, give_feedback() function is called. Then, the function will ask the user to enter name and 
ratings for 5 criterions
```python
1. Cleanliness = int(input("- Cleanliness: "))
2. Room_quality = int(input("- Room quality: "))
3. Staff_service = int(input("- Staff service: "))
4. Price = int(input("- Price: "))
5. Location = int(input("- Location: "))
 
 Each rating must be between 1-5
 if 1 <= Cleanliness <= 5:
                break
            else:
                print("Invalid input! Please rating from 1 - 5!")
```
 the same process is used for other criterions

- Next, the program calculates the average:
average = (Location + Price + Staff_service + Room_quality + Cleanliness) / 5 

- Classify the feedback
```python
if average >= 4.5 :
        level = "Excellent Feedback"
    elif average >= 3.5:
        level = "Average Feedback"
    else:
        level = "Poor Feedback"
```
- Store the feedback
## store value
```python
    feedback = {"Guest Name": guest_name,
                "Cleanliness": Cleanliness, 
                "Room quality": Room_quality,
                "Staff service": Staff_service,
                "Price":Price,
                "Location":Location,
                "average":average,
                "level": level}
    feedbacks.append(feedback)
```
**View feedback**
When the user choose 2, it'll display the feedbacks has been stored

** Feedback report **
When the user choose 3, the report calculates the average for each criterion to identify the strongest and weakest

** Exit **
When the user choose 4, the program exits
```python
 elif choice == "4":
        print("\n --- Thank you for using the service! ---")
        print("=============================================")
        break 
```
## DEMO
```text
Choose: 1
=============================================
           ---- GIVE FEEDBACK ----

- Guest name: Châu
Please rating from 1 - 5 

- Cleanliness: 4

- Room quality: 5

- Staff service: 3

- Price: 5

- Location: 7
Invalid input! Please rating from 1 - 5!

- Location: 3

- The overall satisfaction feedback: 4.0
- Feedback types: Average Feedback

                Thank You
=============================================
```


### 4. Main features
- Collecting feedbacks from 1-5 accross criterions
- Calculates and Classifies overall satisfaction
- Built with Python and requires no external libraries.