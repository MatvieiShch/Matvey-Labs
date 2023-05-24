import math

def calculate_estimate(a, m, b):
    # Розрахунок оцінки завдання
    task_estimate = (a + 4 * m + b) / 6
    # Розрахунок стандартного відхилення завдання
    task_sd = (b - a) / 6
    return task_estimate, task_sd

def calculate_project_estimate(tasks):
    task_estimates = []
    task_sds = []

    # Розрахунок оцінки і стандартного відхилення для кожного завдання
    for task in tasks:
        a, m, b = task
        task_estimate, task_sd = calculate_estimate(a, m, b)
        task_estimates.append(task_estimate)
        task_sds.append(task_sd)

    # Розрахунок оцінки проекту
    project_estimate = sum(task_estimates)
    # Розрахунок стандартного відхилення проекту
    project_sd = math.sqrt(sum(sd**2 for sd in task_sds))

    # Розрахунок 95% довірчого інтервалу
    ci_min = project_estimate - 2 * project_sd
    ci_max = project_estimate + 2 * project_sd

    return project_estimate, ci_min, ci_max

def main():
    tasks = []
    while True:
        # Запитуємо користувача про оцінки для кожного завдання
        a = float(input("Введіть оцінку a: "))
        m = float(input("Введіть оцінку m: "))
        b = float(input("Введіть оцінку b: "))
        tasks.append((a, m, b))

        choice = input("Бажаєте додати ще одне завдання? (Так/Ні): ")
        if choice.lower() != 'так':
            break

    # Розрахунок оцінки проекту та довірчого інтервалу
    project_estimate, ci_min, ci_max = calculate_project_estimate(tasks)

    # Виведення результатів
    print(f"Project's 95% confidence interval: {ci_min} ... {ci_max} points")

if __name__ == '__main__':
    main()
