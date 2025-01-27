# assg5
OOP
'''Create a class representing books
add attributes and methods
use objects to initialize each objec with unique values
add an inheritance layer to explore polymorpism or encapsulation'''


class smartphone:
    def __init__(self,brand:str,model:str,storage_gb:int,color:str):
        self.brand=brand
        self.model=model
        self.storage_gb=storage_gb
        self.color=color
        self.battery_level=100

    def display_inf(self):
        print(f"brand:{self.brand}")
        print(f"model:{self.model}")
        print(f"color:{self.color}")
        print(f"batteryLevel:{self.battery_level}%")
        
   
           
    def charge(self,percentage: int):
        if 0<=percentage<=100:
            self.battery_level +=percentage
            if self.battery_level>100:
                self.battery_level=100
                print("Battery full!")
        else:
            print(f"Battery level after charging:{self.battery_level}")

samsung=smartphone(brand='samsung',model='galaxy 12',storage_gb=256,color='pink')
redmi=smartphone(brand='redmi',model='air 13',storage_gb=128,color='black')

samsung.display_inf()
print()

redmi.charge(79)
redmi.display_inf()


'''Create a program that includes animals or vehicles with the same action (like move()). 
However, make each class define move() differently (for example, Car.move() prints "Driving" 🚗, while Plane.move() prints "Flying" ✈️).'''



class Animal:
    def __init__(self, name):
        self.name = name

    def move(self):
        print("Moving")


class Dog(Animal):
    def move(self):
        print("Running")


class Horse(Animal):
    def move(self):
        print("Galloping")


class Rabbit(Animal):
    def move(self):
        print("Hopping")


class Car:
    def move(self):
        print("Driving")


class Plane:
    def move(self):
        print("Flying")


# Create objects
dog = Dog("Poppy")
horse = Horse("sparrow")
rabbit =Rabbit ("Bunny")
car = Car()
plane = Plane()

dog.move() 
horse.move()  
rabbit.move()  
car.move()  
plane.move()
