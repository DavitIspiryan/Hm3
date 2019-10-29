# Hm3


class Classroom:

    def  __init__(self, roomnumber, numberofseats):
        self.roomnumber = roomnumber
        self.numberofseats = numberofseats
        self.schedule = []

    def getClassRoomInfo(self):
        print("Room Number: ",self.roomnumber)
        print("Number of Seats: ",self.numberofseats)

    def isValid(self, start, end):
        for key in self.schedule:
            if not(end < key["start"] or start > key["end"]):
                return False
        return True

    def reserve(self, start, end):
        if(self.isValid(start,end)):
            timeslot ={"start":start,"end":end}
            return True
        else:
            return False

def main():
    R no1 = Classroom(2,4)
    choice ="?"
    while choice = "not right now":
        choice = input("Would you like to add to schedule (sure, not right now): ")
        if choice == "sure":
            start = int(input("Please enter the start time: "))
            end = int(input("Please enter the end time: "))

            while not(R no1.reserve(start,end)):
                print("Booked, choose another")
                start = int(input("Please enter the start time: "))
                end = int(input("Please enter the end time: "))
        elif choice =="not right now":
            print("Thank you for using openroom.am")
        else:
            print("Invalid input, please try again")
    print(r1.schedule)

main()
