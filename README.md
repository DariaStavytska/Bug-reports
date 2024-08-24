# Bug-reports

![img](https://github.com/DariaStavytska/Bug-reports/blob/main/%D0%BF%D1%80%D0%B8%D0%BA%D0%BB%D0%B0%D0%B4.png)

Баг-репорт – це технічний документ, що описує ситуацію або послідовність дій, що призвела до некоректної роботи об’єкта тестування, з вказанням причин і очікуваного результату. 

Основні атрибути баг-репорта.

1)Summary (Тема)
Перший атрибут, який прописує тестувальник – це короткий опис бага (Summary).

У цьому полі необхідно коротко викласти суть бага. Для того, щоб в повній мірі описати баг, необхідно послідовно відповісти на три питання: ЩО не так працює? в якому місці продукту, тобто ДЕ? і КОЛИ дана проблема з’являється?
Наприклад:
Обов’язкові поля для заповнення не відмічені на формі реєстрації після натискання на кнопку «Надіслати».

2)Description (Детальний опис)

В баг-трекері Mantis це поле використовується для більш широкого опису суті бага, якщо є така необхідність. У всіх інших популярних баг-трекерах (Jira, Redmine) поле Description використовується для опису Кроків для відтворення та фактичного/очікуваного результатів.
В баг-трекері Mantis ці атрибути (кроки і результати) описуються в поле «Steps to reproduce».

3)Steps To Reproduce (Кроки для відтворення)

Необхідно точно описати всі кроки, щоб можна було без проблем відтворити помилку.
Приклад:
Перейти на сайт (посилання на сайт)
Натиснути на кнопку «Реєстрація»
Натиснути на кнопку «Надіслати»
Звернути увагу на форму реєстрації.

На випадок, якщо кроків для відтворення буде дуже багато (більше 8) , можна вказати передумови (Preconditions), наприклад:
Користувач авторизований у системі.
Товар був доданий до кошика.

4)Actual/Expected Result (Результати)

Actual result (Фактичний результат) – вказується що працює не так, в якому місці продукту і за яких умов (тобто, описуючи фактичний результат необхідно знову-таки відповісти на три питання Що? Де? Коли?). По суті, як правило, фактичний результат повинен бути аналогічний Summary.
Expected result (Очікуваний результат) – вказується, як саме має працювати система на думку тестувальника, наприклад: 
Обов'язкові поля для заповнення відмічені на формі реєстрації після натискання на кнопку «Надіслати».

5)Attachments (Вкладення)

До баг-репортів потрібно прикріплювати файли, наприклад, скріншот, відео або лог-файл. Це робиться тому, що інформація краще засвоюється візуально, ніж текстово. Якщо додавати скріншот, де візуально показати стрілкою, що «ось тут баг», то, відкривши цей скріншот іноді можна і не читати кроки і description.
Бувають такі баги, коли скріншот не підтверджує наявність дефекту. В такому випадку, необхідно обов'язково прикріпити і скріншот, і відео з помилкою. Це потрібно для того, щоб візуально зорієнтувати в якому місці шукати баг і не переглядати відео кілька разів.

6)Priority (Пріоритет дефекта)
Це атрибут, що вказує на чергу виконання задачі або усунення дефекту. Можна сказати, що це інструмент менеджера по плануванню роботи. Чим вище пріоритет, тим швидше необхідно усунути дефект. 

Один з варіантів градації Пріоритета дефекту:

P1 Високий (High)
Помилка повинна бути виправлена якомога швидше, адже, її наявність є критичною для проєкту.

P2 Середній (Medium)
Помилка повинна бути виправлена, її наявність не є критичною, але потребує обов’язкового вирішення.

P3 Низький (Low)
Помилка має бути виправлена, її наявність не є критичною, і не потребує термінового усунення. 
Порядок усунення помилок по їх пріоритетам:: High -> Medium -> Low

7)Severity (Серйозність дефекта)  
Це атрибут, що охарактеризовує вплив дефекту на працездатність додатку.

Один з варіантів градації Серйозності дефекту:
S1 Блокер (Blocker)
Блокуюча помилка, що призводить додаток в неробочий стан, в результаті якого подальша робота з тестованою системою або її ключовими функціями стає неможливою. Рішення проблеми необхідне для подальшого функціонування системи.
S2 Критична (Critical)
Критична помилка, неправильно працює ключова бізнес-логіка, діра в системі безпеки, проблема, яка призвела до тимчасового падіння сервера або приводить в неробочий стан деяку частину системи, без можливості вирішення проблеми, використовуючи інші вхідні точки. Рішення проблеми необхідно для подальшої роботи з ключовими функціями тестованою системою.
S3 Значна (Major)
Значна помилка, яка означає, що частина основної бізнес-логіки не працює правильно. Помилка не є критичною, або є можливість роботи з функцією що тестується, використовуючи інші вхідні точки. 
S4 Незначна (Minor)
Незначна помилка, що не порушує бізнес логіку частини додатку, що тестується, очевидна помилка користувацького інтерфейсу.
S5 Незручність (Tweak)
Незручність, очевидна проблема користувацького інтерфейсу. Означає, що необхідний «підгін», підвищення ступеню приязності інтерфейсу.
S6 Текст/одрук (Text)
Невелика текстова помилка/друкарська помилка. Пунктуаційна або орфографічна помилка.
S7 Тривіальна (Trivial)
Проблема, яка не стосується бізнес-логіки додатку, рідко відтворюється, малопомітна в користувацькому інтерфейсі. Помилка сторонніх бібліотек або сервісів, або яка не впливає на загальну якість продукту.

*0 Status (Статус)
Основний атрибут, що визначає поточний стан бага. Відображає життєвий цикл бага від початкового стану до завершення. 
Назви статусів дефектів можуть бути різними в різних баг-трекінгових системах.

9)Оточення дефекта
Component (Компонент) або Environment (Оточення) – це атрибут дефекту, який вказує на якій платформі цей дефект відтворюється (iOS, Android, Windows, Mac і їх версії, назви і версії браузерів, в яких відтворюється дефект). У Mantis оточення вказується в полях «Platform» (назва і версія браузера, PC або Mobile), «OS» (назва операційної системи) і «OS Version» (версія операційної системи).

Також варто вказати другорядні атрибути баг-репорта :
Fix Version (Версія) – цей атрибут вказує, на якому етапі розробки програмного продукту був знайдений дефект. 
Assignee (Призначення) – це атрибут, у якому вказується кому присвоюється баг-репорт для подальшої перевірки.
Build (Номер збірки) – це атрибут, у якому вказаний номер білда, у якому був знайдений дефект. 
Label (Лейбл) – це атрибут, що вказує на належність дефекту до того або іншого типу дефектів (графічний дефект, дефект локалізації і т.д.).
