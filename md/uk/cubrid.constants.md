---
navigation:
  - cubrid.resources.md: « Типи ресурсів
  - cubrid.examples.md: Приклади »
  - index.md: PHP Manual
  - book.cubrid.md: CUBRID
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

Наступні константи можна використовувати під час створення SQL-запросов. Для цього їх можна задати у функціях [cubridprepare()](function.cubrid-prepare.md) і [cubridexecute()](function.cubrid-execute.md)

**Прапори виконання SQL-запиту CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDINCLUDEOID | Визначає, чи отримувати OID під час запиту. |
| CUBRIDASYNC | Запуск запиту асинхронному режимі. |
| CUBRIDEXECQUERYALL | Запуск запиту у синхронному режимі. Цей прапор необхідно встановлювати, коли виконуються множинні SQL-запити. |

Наступні константи використовуються при отриманні результатів. Їх можна задавати у функціях [cubridfetch()](function.cubrid-fetch.md) і [cubridfetcharray()](function.cubrid-fetch-array.md)

**Прапори вилучення CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDNUM | Отримати результат як індексованого масиву (перший індекс 0). |
| CUBRIDASSOC | Отримати результат як асоціативного масиву. |
| CUBRIDBOTH | Отримати результат у вигляді індексованого та асоціативного масивів (за замовчуванням). |
| CUBRIDOBJECT | Отримати результат як об'єкта. |
| CUBRIDЛОБ | Константа CUBRIDLOB може бути використана під час роботи з LOB об'єктами. Її можна задати у функціях [cubridfetch()](function.cubrid-fetch.md) [cubridfetchrow()](function.cubrid-fetch-row.md) [cubridfetcharray()](function.cubrid-fetch-array.md) [cubridfetchassoc()](function.cubrid-fetch-assoc.md) і [cubridfetchobject()](function.cubrid-fetch-object.md) |

Наступні константи використовуються при позиціонуванні курсору в результуючому наборі. Вони передаються та повертаються функцією [cubridmovecursor()](function.cubrid-move-cursor.md)

**Прапори позиціонування курсору CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDCURSORFIRST | Перемістити поточні курси на перший запис. |
| CUBRIDCURSORCURRENT | Переміщати курсор щодо його поточної позиції. Використовується за промовчанням. |
| CUBRIDCURSORLAST | Перемістити поточні курси на останній запис. |
| CUBRIDCURSORSUCCESS | Повертається функцією [cubridmovecursor()](function.cubrid-move-cursor.md) у разі успішного виконання. Прапор видалено з версії 8.4.1. |
| CUBRIDАЛЕMOREDATA | Повертається функцією [cubridmovecursor()](function.cubrid-move-cursor.md) у разі виникнення помилки. Прапор видалено з версії 8.4.1. |
| CUBRIDCURSORERROR | Повертається функцією [cubridmovecursor()](function.cubrid-move-cursor.md) у разі виникнення помилки. Прапор видалено з версії 8.4.1. |

Наступні константи використовуються для визначення режиму автоматичного підтвердження транзакцій. Встановлюються у функції [cubridsetautocommit()](function.cubrid-set-autocommit.md) або повертаються [cubridgetautocommit()](function.cubrid-get-autocommit.md)

**Прапори автопідтвердження транзакцій CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDAUTOCOMMITTRUE | Дозволити режим автоматичного підтвердження транзакції. |
| CUBRIDAUTOCOMMITFALSE | Заборонити автоматичне підтвердження транзакції. |

Наведені нижче константи можна використовувати для встановлення параметрів бази даних. Використовуються у функції [cubridsetдбparameter()](function.cubrid-set-db-parameter.md)

**Прапорці параметрів бази даних CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDPARAMISOLATIONLEVEL | Рівень ізоляції для з'єднання. |
| CUBRIDPARAMLOCKTIMEOUT | Час очікування транзакцій. |

Наступні константи використовуються для визначення рівня ізоляції для транзакцій. Задаються в [cubridsetдбparameter()](function.cubrid-set-db-parameter.md) і повертаються з [cubridgetдбparameter()](function.cubrid-get-db-parameter.md)

**Прапори рівня ізоляції транзакції CUBRID**

| Константа | Описание |
| --- | --- |
| TRANCOMMITCLASSUNCOMMITINSTANCE | Найнижчий рівень ізоляції (1). Може статися брудне, неповторне або фантомне читання для кортежу і читання для таблиці, що не повторюється. |
| TRANCOMMITCLASSCOMMITINSTANCE | Відносно низький рівень ізоляції (2). Брудного читання не буде, але неповторне або фантомне може статися. |
| TRANREPCLASSUNCOMMITINSTANCE | Стандартний рівень ізоляції CUBRID (3). Може статися брудне, неповторне або фантомне читання для кортежу, але гарантується повторюваність читання для таблиць. |
| TRANREPCLASSCOMMITINSTANCE | Відносно низький рівень ізоляції (4). Брудного читання не буде, але неповторне або фантомне може статися. |
| TRANREPCLASSREPINSTANCE | Відносно високий рівень ізоляції (5). Брудного та неповторного читання не буде, але фантомне може статися. |
| TRANSERIALIZABLE | Найвищий рівень ізоляції (6). Ні брудного, ні фантомного, ні читання, що не повторюється, не відбудеться. |

Наступні константи використовують при отриманні схеми бази даних. Використовуються у функції [cubridschema()](function.cubrid-schema.md)

**Прапори схеми CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDSCHCLASS | Отримати ім'я та тип таблиці CUBRID. |
| CUBRIDSCHVCLASS | Отримати ім'я та тип подання CUBRID. |
| CUBRIDSCHQUERYSPEC | Отримати SQL-код, яким створено уявлення. |
| CUBRIDSCHATTRIBUTE | Отримати атрибути стовпця таблиці. |
| CUBRIDSCHCLASSATTRIBUTE | Отримати атрибути таблиці. |
| CUBRIDSCHMETHOD | Отримати метод екземпляра. Метод екземпляра - це метод, який викликається екземпляром класу. Він використовується частіше, ніж метод класу, оскільки більшість операцій запускаються усередині екземпляра. |
| CUBRIDSCHCLASSMETHOD | Отримати метод класу. Метод класу – це метод, що викликається об'єктом класу. Зазвичай використовується для створення нового екземпляра класу або його ініціалізації. Також він використовується для доступу до атрибутів класу та їх зміни. |
| CUBRIDSCHMETHODFILE | Отримати інформацію про файл, у якому визначено метод таблиці. |
| CUBRIDSCHSUPERCLASS | Отримати ім'я та тип таблиці, з якої успадковуються атрибути. |
| CUBRIDSCHSUBCLASS | Отримати ім'я та тип таблиці, у якій успадковуються атрибути поточної таблиці. |
| CUBRIDSCHCONSTRAINT | Отримати обмеження таблиці. |
| CUBRIDSCHTRIGGER | отримати тригер таблиці. |
| CUBRIDSCHCLASSPRIVILEGE | Отримати інформацію про права доступу до таблиці. |
| CUBRIDSCHATTRPRIVILEGE | Отримати інформацію про права доступу до стовпця таблиці. |
| CUBRIDSCHDIRECTSUPERCLASS | Отримати таблицю, яка є прямим предком цієї. |
| CUBRIDSCHPRIMARYKEY | Отримати первинний ключ таблиці. |
| CUBRIDSCHIMPORTEDKEYS | Отримати імпортовані ключі таблиці. |
| CUBRIDSCHEXPORTEDKEYS | Отримати експортовані ключі таблиці. |
| CUBRIDSCHCROSSREFERENCE | Отримати зв'язки двох таблиць. |

Наступні константи використовуються для позначення помилок. Вони можуть бути повернуті функцією [cubriderrorcodefacility()](function.cubrid-error-code-facility.md)

**Коди помилок CUBRID**

| Константа | Описание |
| --- | --- |
| CUBRIDFACILITYDBMS | Виникла помилка в CUBRID dbms. |
| CUBRIDFACILITYCAS | Виникла помилка в cas брокера CUBRID. |
| CUBRIDFACILITYCCI | Виникла помилка в CUBRID cci. |
| CUBRIDFACILITYCLIENT | Виникла помилка в клієнті PHP CUBRID. |
