calls_list = [["Medical Call", "19"], ["Check In", 
"14"], ["Medicine Reminder", "7"], ["Check In", "14"], ["Fire Alarm", "18"]]

#Edit This List to make the Queue:
#The list only needs to contain name of the calls, not the priority.
correct_list = []
correct_list.append(calls_list[0][0])
correct_list.append(calls_list[4][0])
correct_list.append(calls_list[3][0])
correct_list.append(calls_list[1][0])
correct_list.append(calls_list[2][0])

#Print out the Queue using the pop function.
#Expected output: Medical Call, Fire Alarm, Check In, Check In, Medicine Reminder
for i in range(0, len(correct_list)):
    print(correct_list.pop(0))