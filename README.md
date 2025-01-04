# Тема 4. Домашня робота. Робота з датою, часом та розширена робота з рядками

## Завдання 1

Створіть функцію `get_days_from_today(date)`, яка розраховує кількість днів між заданою датою і поточною датою.


## Завдання 2

Щоб виграти головний приз лотереї, необхідний збіг кількох номерів на лотерейному квитку з числами, що випали випадковим чином і в певному діапазоні під час чергового тиражу. Наприклад, необхідно вгадати шість чисел від 1 до 49 чи п'ять чисел від 1 до 36 тощо.

Вам необхідно написати функцію `get_numbers_ticket(min, max, quantity)`, яка допоможе генерувати набір унікальних випадкових чисел для таких лотерей. Вона буде повертати випадковий набір чисел у межах заданих параметрів, причому всі випадкові числа в наборі повинні бути унікальні.


## Завдання 3

У вашій компанії ведеться активна маркетингова кампанія за допомогою SMS-розсилок. Для цього ви збираєте телефонні номери клієнтів із бази даних, але часто стикаєтеся з тим, що номери записані у різних форматах. Наприклад:

```bash
" +38(050)123-32-34"
" 0503451234"
"(050)8889900"
"38050-111-22-22"
"38050 111 22 11 "
```

Ваш сервіс розсилок може ефективно відправляти повідомлення лише тоді, коли номери телефонів представлені у коректному форматі. Тому вам необхідна функція, яка автоматично нормалізує номери телефонів до потрібного формату, видаляючи всі зайві символи та додаючи міжнародний код країни, якщо потрібно.

Розробіть функцію `normalize_phone(phone_number)`, що нормалізує телефонні номери до стандартного формату, залишаючи тільки цифри та символ `'+'` на початку. Функція приймає один аргумент - рядок з телефонним номером у будь-якому форматі та перетворює його на стандартний формат, залишаючи тільки цифри та символ `'+'`. Якщо номер не містить міжнародного коду, функція автоматично додає код `'+38'` (для України). Це гарантує, що всі номери будуть придатними для відправлення SMS.


## Завдання 4

У межах вашої організації, ви відповідаєте за організацію привітань колег з днем народження. Щоб оптимізувати цей процес, вам потрібно створити функцію `get_upcoming_birthdays`, яка допоможе вам визначати, кого з колег потрібно привітати. Функція повинна повернути список всіх у кого день народження вперед на 7 днів включаючи поточний день.

У вашому розпорядженні є список `users`, кожен елемент якого містить інформацію про ім'я користувача та його день народження. Оскільки дні народження колег можуть припадати на вихідні, ваша функція також повинна враховувати це та переносити дату привітання на наступний робочий день, якщо необхідно.

```bash
users = [
    {"name": "Jack", "birthday": "1982.04.27"},
    {"name": "Evan", "birthday": "2000.06.25"},
    {"name": "Tom", "birthday": "1995.04.25"},
    {"name": "Mac", "birthday": "1972.01.01"},
]
```