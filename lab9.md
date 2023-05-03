#backend code 
class Person:
    def __init__(self, name, age, occupation):
        self.name = name
        self.age = age
        self.occupation = occupation
        
class House:
    def __init__(self, address, number_of_rooms, area):
        self.address = address
        self.number_of_rooms = number_of_rooms
        self.area = area
        self.residents = []
    
    def add_resident(self, person):
        self.residents.append(person)
        
    def remove_resident(self, person):
        self.residents.remove(person)
        
    def print_residents(self):
        print("Residents of the house ",self.address, "having area ", self.area ,"and ", self.number_of_rooms, "rooms.")
        for resident in self.residents:
            print(f"\t{resident.name}, age {resident.age}, occuaption {resident.occupation}")



#output code 
# Person objects
person1 = Person("Ahmad", 19, "undergraduate computer student", )
person2 = Person("Nehal", 24, "undergraduate literature student")
person3 = Person("Ansa", 19, "undergradutes mass com student")

# House object 
house = House("200 hundered rivers bend circle, Chester VA", 9, "19 acres")
#adding resident 
house.add_resident(person2)
house.add_resident(person1)

# resident print
house.print_residents()

# Removoing and adding a resident and printing out the updated list of residents
house.remove_resident(person1)
house.add_resident(person3)
house.print_residents()
