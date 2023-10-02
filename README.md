from random import randint

# number = randint(1, 9)
#
# trynum = 3
#
# print("Угадай число!")
# print("Случайное число находится между 1 и 9")
# print("У Вас есть 3 попытки, ИГРА НАЧИНАЕТСЯ!")
#
#
# for _ in range(trynum):
#     try:
#
#         first = int(input("Попытка , введите свое загаданное число:"))
#
#         if first == number:
#             print("Поздравляем! Вы угадали число!")
#             break
#         else:
#             print("Не угадали. У вас осталось", trynum - 1, "попыток.")
#             trynum -= 1
#     except ValueError:
#         print("Пожалуйста, введите число.")
#
#
# else:
#     print("К сожалению Вы использовали все 3 попытки и проиграли! ")


#
# import random
#
#
# variant = ["камень", "ножницы", "бумага"]
#
#
# index = random.randint(1, 3)
# computer= variant[index]
#
# user= input("Выберите: камень, ножницы или бумага: ").lower()
#
#
# if user not in variant:
#     print("Пожалуйста, выберите один из следующих вариантов: камень, ножницы или бумага.")
# else:
#     print("Компьютер выбрал:", computer)
#     print("Вы выбрали:", user)
#
#
#     if user == computer:
#         print("Ничья!")
#     elif (
#         (user == "камень" and computer == "ножницы")
#         or (user == "ножницы" and computer == "бумага")
#         or (user == "бумага" and computer== "камень")
#     ):
#         print("Вы выиграли!")
#     else:
#         print("Компьютер выиграл!")

# def determine_operator(phone_number):
#     phone_number = str(phone_number)
#
#     operator_prefixes = {
#         "Activ": ["700", "708"],
#         "Beeline": ["701", "702"],
#         "Kcell": ["705", "771", "776", "777"],
#         "Tele2": ["707", "747"],
#     }
#
#     for operator, prefixes in operator_prefixes.items():
#         for prefix in prefixes:
#             if phone_number.startswith(prefix):
#                 return operator
#
#     return "Неизвестный оператор"
#
# try:
#     phone_number = int(input("Введите номер телефона (без +7/8): "))
#     operator = determine_operator(phone_number)
#     if operator != "Неизвестный оператор":
#         print(f"Номер относится к оператору {operator}")
#     else:
#         print("Не удалось определить оператор")
# except ValueError:
#     print("Введите номер телефона ")



def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Деление на ноль невозможно"
    return x / y

def calculator():
    print("Доступные операции:")
    print("1. Сложение (+)")
    print("2. Вычитание (-)")
    print("3. Умножение (*)")
    print("4. Деление (/)")

    choice = input("Выберите операцию (1/2/3/4): ")

    if choice in ('1', '2', '3', '4'):
        num1 = float(input("Введите первое число: "))
        num2 = float(input("Введите второе число: "))

        if choice == '1':
            result = add(num1, num2)
            operation = "Сложение"
        elif choice == '2':
            result = subtract(num1, num2)
            operation = "Вычитание"
        elif choice == '3':
            result = multiply(num1, num2)
            operation = "Умножение"
        else:
            result = divide(num1, num2)
            operation = "Деление"

        print(f"Операция: {operation}")
        print(f"Результат: {result}")
    else:
        print("Некорректная операция")

if __name__ == "__main__":
    calculator()
