# #### Q1 - What are conventions/rules for naming Python variables?
To assign a name to a Python variable, the user must associate it with a value. For instance, the code snippet "x = 8" assigns the value 8 to the variable x. When creating a variable in Python, there's no obligation to explicitly declare a specific type. However, developers have the option to specify a data type using the casting function. If a user desires a string representation, the 'str()' function is employed. For integers, the 'int()' function is utilized, while 'float()' is used for floating-point numbers.



# #### Q2 - What are the two main numeric data types in Python?
Floats and Integers 


# #### Q3 - Why are data types important?
Data types play a crucial role as they instruct the computer system on how to interpret data values accurately. They serve to guarantee that data is gathered in the intended format, ensuring that each data point holds the expected value


# #### Q4 - How do you check an object’s data type?
 You can  use the type() function


# #### Q5 - Create a string called “Washington D.C.” and assign it to a variable using a name that follows Python conventions.

washdc=str("Washington D.C.") #Created a string called Washington DC
washdc

# #### Q6 - How can you remove the periods from the string you created in #5?
washdc.translate({ord(letter): None for letter in '.'})

# #### Q7 - What are two different ways to access the “W” in “Washington D.C.” with an index?

washdc[0] 
washdc[len(washdc) - 15]

# #### Q8 - Create a list of employee IDs from 100 to 110 incremented by 1

employee_id=list(range(100,111))
employee_id

# #### Q9 - Loop through the list of employee IDs and print “Sales” if the employee is less than 105 and print “Finance” otherwise.

for x in (employee_id):
  if x < 105:
    print("Sales")
    continue
print("Finance")

# #### Q10 - Convert the following scenario to a conditional statement: If a user clicks “buy” print “Thank you for your purchase!

marketing="buy"
marketing
if marketing=="buy":
    print("Thank you for your purchase!")



# #### Q11 - Add to the above conditional statement by printing "Need more time?" if the user does not click buy. Ensure the function returns a value.

marketing="idk" #example where user does not click buy
marketing
if marketing=="buy":
    print("Thank you for your purchase")
else:
     print("Need more time?")


# #### Q12 - Write a for loop that iterates over a list (that you create) of 10 stock prices. In the for loop, add conditions that check the price and print “High”, “Mid”, or “Low” depending on the value. You decide on the prices and values for each condition.

stockprices=list(range(1,11)) #list of stock prices
stockprices
for p in (stockprices):
  if p <= 3: #Low range is less than or equal to 3
    print("low")
  elif p>3 and p<=6 : #mid range is between 4 and 6
    print("medium")
  else:       
    print("high") #high range is greater than 6

# #### Q13 - Define a function that takes a list as an input and returns a new list that contains the first and last element of the input list.

def my_function(fastfood):
    ans=(fastfood[0],fastfood[len(fastfood) - 1])
    print(ans)
 
food=["pizza","fries","salad"]   

my_function(food)


# #### Q14 - Define a function that calculates a business’ debt-to-equity (D/E) ratio given its total liabilities and total equity. Return the result. Ensure the function returns a value.


def steven14(liab,equity):
    ans=int(liab/equity)
    print(ans)
liab=8
equity=2
deratio(liab,equity)


# #### Q15 - Adjust the function you defined in #14 to return “Warning” if the result is greater than 2 and “OK” otherwise. Test your function to ensure it works.

def steven14(liab,equity):
    ans=int(liab/equity)
    if ans>2:
        print("Warning")
    else:
        print("Ok")
    
liab=4
equity=2
deratio(liab,equity)


# #### Q16 - What is scope and why is it important?
A scope refers to the context where a variable is exclusively accessible, limited to the area in which it is created. For instance, if a variable is defined within a function, its relevance is confined to and influences computations solely within that specific function. This distinction is crucial as it dictates the precise location in your program code where a name is recognizable by the Python system. Scopes are essentially implemented as dictionaries that establish a mapping between names and corresponding objects.


# #### Q17 - Define a function with a local variable called “base_amount” that takes the value of 50 and takes two inputs, computes the sum of base amount and the two inputs, and then multiples that sum by “base_amount.” Run the code with inputs to ensure it works.


def steven17(input1,input2):
    base_amount=50
    ans=(base_amount+input1+input2)*base_amount
    print(ans)

steven17(1,2)

# #### Q18 - Try to print “base_amount” in your global environment. What happens? What does Python tell you?

print(base_amount)

# #### Q19 - What are classes?
A class operates akin to a "template" for generating objects. When a class is instantiated, it establishes a local namespace encompassing all its attributes, including both data and functions defined within it.


# #### Q20 - Create a class called User with three attributes: id, lastname, balance. Create three instances of the User class called user1, user2, user3. Print the last name of user1 and the balance of user2, using an f-string.

class User:
    def __init__(user,ID,lastname,balance):
        user.lastname=lastname
        user.balance=balance
        user.ID=id 
 
user1=User(1,"smith",2)
user2=User(2,"han",3)
user3=User(3,"Jonas",4)

f"The last name of User 1 is: {user1.lastname} and the balance of user 2 is:({user2.balance})"

# #### Q21 - What is the command line? Explain what each of the following command line commands do: ls, pwd, cd, mkdir
A command line is a user interface accessed by entering text commands. This approach is particularly handy when automating tasks or executing them remotely. For instance, the command 'ls' provides a list of all files and directories in the current working directory. Similarly, 'pwd' outputs the name of the working directory, 'cd' facilitates moving up one directory, and 'mkdir' accepts a directory name as an argument, creating a new directory within the current working directory.

# Q22 - What is git (in your own words)? Explain what each of the following git command line commands do: git init, git status, git add, git commit, git push
Git serves as a version control system adept at managing file changes. When you save in Git, it swiftly captures a snapshot of all files, providing users with a comprehensive repository copy rather than relying on a central server for access.
 Here are explanations for some essential Git commands:
1. git init: Initiates a new repository, facilitating the incorporation of new projects or the conversion of existing projects into the repository.
2. git status: Displays the status of the staging area and the working directory. It allows users to visualize untracked files and changes that are not yet staged.
#3. git add: Adds a change to the staging area, although it does not significantly impact the repository.
#4. git commit: Captures a snapshot of the staged changes in the project, essentially creating a "save checkpoint" that proves invaluable for debugging.
#5. git push: An integral part of the overall Git synchronization process, it publishes local changes to a central repository.


# #### Q23 - What is a virtual environment and why is it useful for deploying Python applications?
Virtual environments serve as collaborative workspaces, fostering a shared platform for various projects. This proves highly beneficial when deploying Python applications as it effectively isolates each project along with its dependencies. In practical scenarios, it's common to engage in multiple projects concurrently, often developed with different tools. Utilizing a virtual environment becomes essential in such cases to prevent debugging errors and ensure seamless project isolation


# Q24 - What is the difference between git and GitHub? Is it possible to use git without using GitHub?

Git empowers us to effectively manage and track the history of source code, while GitHub, a cloud-based hosting service, facilitates repository management, particularly for open-source projects. It's crucial to note that Git can be used independently of GitHub. GitHub extends the capabilities of Git by providing additional resources, enhanced functionality, and a dedicated platform for storing and collaborating on projects. In essence, GitHub takes Git a step further, offering a robust ecosystem for developers.

# Q25 - What is a list comprehension? Write a for loop that returns a new list with the cube of 2, 3 and 4. Write a list comprehension that does the same thing

beforecube = [2,3,4]
newlist = []

for x in beforecube:
    newlist.append(pow(x,3))
print(newlist)

newlist2=[pow(x,3) for x in newlist]
