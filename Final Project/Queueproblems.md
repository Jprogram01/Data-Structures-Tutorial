# Problem One

Create a grocery list, where you grab items in order of the queue. The priority of each item is as follows: Medicine, Food, Cleaning. Make a queue in order with two items from each category.



## Solution: 
grocery_list = []
for i in range(1,7):
    item = input("Add an item ")
    grocery_list.append(item)
print(grocery_list)
    
















# Problem two

You are tasked with setting up the queue for a call center. You are given a list of lists. Those different list that have different types of calls and the priorities that come with them. The higher a priority the sooner the call should be taken. If a call has equal priority with another class it does not matter the order in which the call is as long as its above priorities below it and below priorities above it.


#These are the calls given
calls_list = [["Medical Call", "19"], ["Check In", "14"], ["Medicine Reminder", "7"], ["Check In", "14"], ["Fire Alarm", "18"]]

#Edit This List to make the Queue:
#The list only needs to contain name of the calls, not the priority.
correct_list = []


#Print out the Queue using the pop function.
#Expected output: Medical Call, Fire Alarm, Check In, Check In, Medicine Reminder



(Solution)[Final Project/QueueSolution.md]



