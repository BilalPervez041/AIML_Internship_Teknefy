# oop four pillors code.
from abc import ABC, abstractmethod
# 1. Abstraction + Encapsulation
class Vehicle(ABC):
    def __init__(self, brand, model):
        self.__brand = brand    # encapsulation (private variable)
        self.__model = model
    @abstractmethod
    def display(self):          # abstraction
        pass
    def get_info(self):
        return f"{self.__brand} {self.__model}"
# 2. Inheritance
class Car(Vehicle):
    def display(self):
        return "This is a Car."
# 3. Polymorphism
class Bike(Vehicle):
    def display(self):
        return "This is a Bike."
# Using the classes
car = Car("Toyota", "Corolla")
bike = Bike("Honda", "125")
print(car.get_info(), ":", car.display())
print(bike.get_info(), ":", bike.display())




 



