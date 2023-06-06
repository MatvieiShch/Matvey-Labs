from converter import convert_number_to_words

def main():
    name = input("Введіть своє ім'я: ")
    print(f"Привіт, {name}!")
    number = int(input("Введіть число: "))
    words = convert_number_to_words(number)
    print(f"Словесне представлення числа {number}: {words}")

if name == "main":
    main()
