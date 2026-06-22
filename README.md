# python-hw-28-tms-

1 Создайте класс "Круг", который имеет атрибуты радиус и цвет, и
методы вычисления площади и длины окружности. Создайте несколько
объектов этого класса и вызовите его методы для каждого объекта.

```
class Circle:
    def __init__(self, color, radius):
        self.color = color
        self.radius = radius
    def square(self):
        return f"Площадь круга {int(self.radius) * int(self.radius) * 3.14}"
    def length(self):
        return f"Длина окружности: {2 * int(self.radius) * 3.14}"

circle = Circle("blue", "10")
print(circle.color)
print(circle.radius)
print(circle.square())
print(circle.length())
```

2 Создайте класс "Банковский счет", который имеет атрибуты номер
счета, имя владельца, баланс и методы пополнения и снятия денег со
счета. Создайте несколько объектов этого класса и вызовите его методы
для каждого объекта.

```
class Bank:
    def __init__(self, name_holder, balans):
        self.name_holder = name_holder
        self.balans = int(balans)


    def replenish(self, amount):
        if amount > 0:
            self.balans += amount
    
    def pay(self, amount):
        if 0 < amount <= self.balans:
            self.balans -= amount

bank = Bank("Nikita", "9999")
bank.replenish(999)
print(f"Person: {bank.name_holder} balans: {bank.balans}")

bank.pay(999)
print(f"Person: {bank.name_holder} balans: {bank.balans}")
```

3 Создайте класс "Студент", который имеет атрибуты имя, возраст и
средний балл. Создайте методы для вычисления среднего балла и
определения статуса студента (отличник, хорошист, троечник).Создайте
несколько объектов этого класса и вызовите его методы для каждого
объекта.

```
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age


    def avg(self, value):
        
        self.avg = sum(value) / len(value)
        return self.avg
    
    def status(self, avg):
        if int(avg) < 5:
            self.__status = "bad"
        if int(avg) > 5:
            self.__status = "good"
        return self.__status

student_bad = Student("Nikita", "29")
student_bad.avg([3, 3, 3, 3, 3])
print (f"Студент {student_bad.name} имеет средний бал {student_bad.avg}.\nСтатус студента {student_bad.status(student_bad.avg)}")

student_good = Student("Vasya", "33")
student_good.avg([7, 7, 7, 7, 7])
print (f"Студент {student_good.name} имеет средний бал {student_good.avg}.\nСтатус студента {student_good.status(student_good.avg)}")
```
