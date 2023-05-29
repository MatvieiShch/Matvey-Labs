def analyze_file(file_path):
    try:
        with open(file_path, 'r') as file:
            lines = file.readlines()
            line_count = len(lines)
            empty_line_count = sum(1 for line in lines if line.strip() == '')
            letter_z_line_count = sum(1 for line in lines if 'z' in line)
            letter_z_count = sum(line.count('z') for line in lines)
            and_line_count = sum(1 for line in lines if 'and' in line)

            print("Статистика файлу:")
            print(f"1. Кількість рядків: {line_count}")
            print(f"2. Кількість порожніх рядків: {empty_line_count}")
            print(f"3. Кількість рядків з літерою 'z': {letter_z_line_count}")
            print(f"4. Кількість літер 'z' у файлі: {letter_z_count}")
            print(f"5. Кількість рядків з групою символів 'and': {and_line_count}")

    except FileNotFoundError:
        print("Файл не знайдено.")
    except IOError:
        print("Помилка відкриття файлу.")


def main():
    while True:
        file_path = input("Введіть шлях до файлу: ")
        analyze_file(file_path)

        choice = input("Бажаєте проаналізувати ще один файл? (Так/Ні): ")
        if choice.lower() != 'так':
            break


if __name__ == '__main__':
    main()
