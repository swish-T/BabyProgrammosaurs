# BabyProgrammosaurs
# All of the baby programs that will eventually become programmosaurs come here to grow.

# Baby program 1: Counts and Averages

# User instructions
print "Enter as many numbers as you like. When you've finished, type 'done' to see the count, sum, and average of your set."
count = None
total = None
while True: 
    # Test for shitty input.
    try: 
        num = raw_input ("Enter a number: ")
        num = float(num)
        
    # Provide cases for loop breaking
    except: 
        if num == 'done' :  break
        if len(num) < 1 : break
        else : 
             print "Invalid input"
             # reprompt user just in case they screwed up on accident
             continue 
    # set up count var         
    if count == None :
        count = 0
    else :     
        count = count + 1
    # set up total var
    if total == None :
        total = num
    else :
        total = total + num
# Just in case the user decides to be a smartass and do the thing before putting numbers in.        
if count == None and total == None and num == 'done' :
    print "all done, no values entered."
else :
    print "all done: ",count,total, total/count
