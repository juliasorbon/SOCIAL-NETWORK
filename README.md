# SOCIAL NETWORK
****
### Даний проєкт є міні-відворенням базових функцій в соц.мережах.
****
>homework разом з `WaRaN1` і `maximbabaiev` :busts_in_silhouette:
****
>:eyes: Усі файли і папки мають бути в одній папці для коректної роботи коду :eyes:

:books: Потрібно встановити: 

| Бібліотекy| Версія | Команди|
|----------------|:---------:|----------------:|
| pymysql| 1.0.1 | import pymysql|
| Easygui | 0.98.3 | from easygui import * |

# Логіка коду :large_blue_diamond:
****
У проєкті є 4 файлa. ___FileStart, Login, AddData___ i ___Main___.

>`Main` - це основний файл, який треба запускати самим першим і єдиним, маючи відкриті на фоні нище перераховані.

>`FileStart` - це файл в якому прописаний код створення датабази.
>При його запуску - вас запитають ваш логін(root) і пароль до SQL. Потім вам створиться database, заповниться таблицями і додасться дефолтний акаунт в таблицю users.

>У дефолтного юзера: `login` буде - ADMIN,а пароль - `1234`

>`Login` - це файл, який буде викликатись наступним. Він перевіряє чи є ви у таблиці users, чи ви ввели правильний логін/пароль - чи маєте акаунт у базі. 

>`AddData` - це файл в якому записані усі функції, імпортувавши його у файл `main` - ми зберегли більше місця і чистоту main.

# Можливості програми :large_blue_diamond:
****
Після того, як ви зайшли у свій акаунт - вам відкривається меню Easygui з великим вибором варіантів для роботи в SQL.\
Усі операції будуть записуватись і проводитись за логіном під яким ви зайшли в мережу.

   ![Alt-текст](https://github.com/juliasorbon/SOCIAL-NETWORK/blob/main/images/11.jpg "interface")

Декілька з доступних функцій:
****
+ `Post` - керування таблицею з постами.
    - Вам висвітлиться віконце _buttonbox_ де ви зможете вибрати наступні дії:
        - `Додати пост`
            - Дати ім'я публікації, написати саму публікацію. Підписом буде ваш логін під яким ви зайшли в мережу :heavy_check_mark: 
        - `Перегляд усіх публікацій`
            - Побачити усі свої публікації. :heavy_check_mark: 
        - `Видалити пост`
            - Видаляти свої пости.  :heavy_check_mark: 
     - Усі дії проводяться через таблицю `Posts`
****
+ `Friends` - керувати друзями.
- Вам висвітлиться віконце _buttonbox_ де ви зможете вибрати наступні дії:
  - `Додати друга` :heavy_check_mark: 
  - `Переглянути своїх друзів`  :heavy_check_mark: 
  - `Видалити друга`  :heavy_check_mark: 
- Усі дії проводяться через таблицю `Friends`. 
- Ви зможете додавати друзів тільки, якщо вони є у нашій database - таблиці `users`.
****
+ `Search`
  - Пошук користувачів по _login_ - вертає інформацію про них у базі.  :heavy_check_mark: 
 - Ці дії проводяться через таблицю `users`
****
+ `Settings`
  -  Реєстрація нового юзера/додавання його в таблицю `users` :heavy_check_mark: 
  -  Редагування вашої інформації :heavy_check_mark: 
  -  Видаляння акаунта по логіну  :heavy_check_mark: 
- Ці дії проводяться через таблицю `users`
****

:exclamation: ***Параметр `login` у таблиці `users` є унікальним і зв'язує усі таблиці між собою.*** \
Ви не зможете створити нового юзера, якщо вибраний вами _login_ вже занятий. 

 :heavy_multiplication_x: _Баг (фіга) коду_ :heavy_multiplication_x: 
>Програма крашниться, якщо ви спробуєте видалити свій акаунт, по логіну під яким ви зайшли :heavy_multiplication_x: 
