# class declaration, modules, and variables
class Hotel_Manage:

    def __int__(self, total_cost='', room_cost='', p=0, food_cost='', t=0, additional_charge=10, address='',
                name='', date_in='', date_out='', room_no=1):

        self.total_cost = total_cost
        self.food_cost = food_cost
        self.t = t
        self.p = p
        self.room_cost = room_cost
        self.address = address
        self.date_in = date_in
        self.date_out = date_out
        self.room_no = room_no

    # entering customer information
    def customer_data(self):
        self.name = input("Enter your full name ")
        self.address = input("Enter your address ")
        self.date_in = input("Enter check-in date ")
        self.date_out = input("Enter check-out data ")

    # defining available rooms and their costs
    def rooms_available(self):
        print("We have the following rooms"
              "1. King's size bed bed ----->$40"
              "2. Queen's size bed ----->$30"
              "3. Single size bed ----->$20")
        room = int(input("Enter the class of rooms you'd like "))
        stay_period = int(input("Enter number of nights you will be staying "))
        if room == 1:
            print("You selected Class 1 rooms")
            self.room_cost = 40 * stay_period
        elif room == 2:
            print("You selected Class 2 rooms")
            self.room_cost = 30 * stay_period
        elif room == 3:
            print("You have selected Class 3 rooms")
            self.room_cost = 20 * stay_period
        else:
            print("Enter room class and stay period")
        print("Your room will cost you $", self.room_cost)
        print("Note that all room prices are exclusive of food and drinks")

    # defining available meals and their costs
    def food(self):
        print("0. Menu"
              "1. Breakfast---->$10"
              "2. Lunch----$20"
              "3. Dinner---->$20"
              "4. Bottle of wine---->$10"
              "5. Glass of whiskey or vodka---->$2")
        while 1:
            food_choice = int(input("Select food from menu "))
            if food_choice == 1:
                number_of_plates = int(input("Enter the number of plates you'd like served "))
                self.food_cost = 10 * number_of_plates
                break
            elif food_choice == 2 or 3:
                number_of_plates = int(input("Enter the number of plates you'd like served "))
                self.food_cost = 20 * number_of_plates
                break
            elif food_choice == 4:
                number_of_plates = int(input("Enter the number of bottles you'd like served "))
                self.food_cost = 10 * number_of_plates
                break
            elif food_choice == 5:
                number_of_plates = int(input("Enter the number of glasses you'd like served "))
                self.food_cost = 2 * number_of_plates
                break
            elif food_choice == (2 or 3) and 4:
                number_of_plates = int(input("Enter the number of plates you'd like served "))
                self.food_cost = (20 * number_of_plates) + 7
                break
            else:
                print("Please enter a valid choice")
                break
        print("Your cost of food is  $", self.food_cost)

    def display(self):
        print("*****Bill****")
        print("Customer details:")
        print("Name: ", self.name)
        print("Address", self.address)
        print("Check-in date: ", self.date_in)
        print("Check-out date: ", self.date_out)
        print("Your room rent is: $", self.room_cost)
        print("Your food bill is: $", self.food_cost)
        self.total_cost = self.food_cost + self.room_cost

        print("Your total cost is: $", self.total_cost)
        print(f"VAT paid is {0.16 * self.total_cost}")
        print("Your grand total is :", self.total_cost + (0.16 * self.total_cost))


def main():
    a = Hotel_Manage()
    print('Welcome to Le Mach Hotel')
    while 1:
        print(
            "1. Enter customer data "
            "2. Calculate room rent "
            "3. Calculate food cost "
            "4. Show total cost "
            "5. Exit")

        b = int(input("Select option: "))
        if b == 1:
            a.customer_data()
        if b == 2:
            a.rooms_available()
        if b == 3:
            a.food()
        if b == 4:
            a.display()
            break
        if b == 5:
            quit()


main()
