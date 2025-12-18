# golden-ratio
# In this code, you can find an approximation of the golden ratio to x decimal places using the Fibonacci sequence. I satrted by writing a code to find the n'th term of the Fibonacci sequence (n being the user's input). Using if statements and for loops helped acheive this in a concise manner I had some problems at first as the code began with the sequence starting at 1 [ 1, 1, 2 etc] even though the sequence begins at 0 [0, 1, 1, 2 etc], therefore I changed the value of a to 0 rather than being 1. I then decided for the next step of my project to use this code to calculate the golden ratio. I had to slightly alter my code by getting a different user input and using more mathematical operators. Initially, the code was printing the same amount of times as the value of 'term' but after adding a break in the for loop and if statement, this issue was resolved. 

#this code finds the user's term of the fibonacci sequence which they input 

a = 0
b = 1


term = int(input("Which term would you like to find out?"))

if term == 1:
    print (0)
if term == 2:
    print (1)
else:
    for i in range (3, term +1):
        c = a + b
        a = b
        b = c
        print (b)


# The aim of this code is to find an approximation of the golden ratio to x decimal places

x = int(input("To how many decimal places would you like to calculate the golden ratio?"))

term = 999999

a = 1
b = 1



for i in range (3, term +1):
    c = a + b
    if abs (b/a - c/b) < 10 ** -x :
        print ("The golden ratio is : " , round(10 ** x *c/b)/10 ** x)
        break   
    a = b
    b = c

