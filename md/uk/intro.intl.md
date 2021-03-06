- [« intl](book.intl.md)
- [Встановлення та налаштування »](intl.setup.md)

- [PHP Manual](index.md)
- [intl](book.intl.md)
-   Вступ

# Вступ

Модуль інтернаціоналізації (далі Intl) - це обгортка для бібліотеки
[» ICU](http://www.icu-project.org/), що дозволяє програмістам на PHP
робити різні операції, які залежать від локалі, наприклад,
форматування, транслітерація, перетворення кодувань, операції з
календарем, сумісне з [»UCA](http://www.unicode.org/reports/tr10/)
порівняння, визначення меж тексту та працювати з ідентифікаторами
локалей, часовими поясами та графемами.

Програмний інтерфейс модуля розробляється так, щоб якомога точніше
повторювати API ICU, щоб люди, які працювали з ICE у C/C++ або Java, могли
легко використовувати API PHP. Також завдяки цьому документація ICE може
бути корисною зрозуміти різниця функції ICU.

Intl складається з кількох модулів, кожен із яких надає
відповідний API ICU:

- Модуль порівняння: надає інструменти для порівняння рядків з
підтримкою відповідного локалі порядку сортування.
- Модуль форматування чисел: дозволяє відображати числа в
відповідно до правил локалі, або заданим шаблоном або з набором
правил. Також дозволяє правильно розбирати рядки у числа.
- Модуль форматування повідомлень: дозволяє створювати повідомлення,
включають дані (такі як числа та дати), відформатовані в
відповідно до заданих шаблонів і локальних правил, і, також,
розбирати повідомлення, витягуючи з них дані.
- Модуль нормалізації: надає функції для перетворення
тексту до однієї з нормалізованих форм Unicode. Також надає
можливість перевірити, чи є наданий текст вже
нормалізованим.
- Модуль локалі: надає взаємодію з ідентифікаторами
локалі як до функцій, дозволяючи отримати вкладені теги локалі;
розбір, композиція, порівняння (пошук та фільтрація) ідентифікаторів
локалі.
- Модуль календаря: надає клас, корисний для проведення
залежних від локалі операцій з календарем, отримання різної
інформації, такої як часові пояси для обраної локалі, перший
день тижня або режим поточного зимового/літнього часу.
- Модуль часового поясу: надає обгортку над [» базою даних часових поясів](http://www.iana.org/time-zones), у якій
міститься вичерпна інформація про всі світові часові пояси.
- Модуль форматування дати: дозволяє відображати дату в
відповідно до прийнятого для даної локалі формату або заданого
шаблоном або набором правил. Також потрібен для розбору рядків,
що містять опис дати та часу.
- Модуль транслітерації: дозволяє отримати подання рядка на
різних мов в латиниці.

## Посилання

- [» Різна документація ICU](http://site.icu-project.org/docs/)

-   [" Посібник користувача ICU](https://unicode-org.github.io/icu/userguide/)

- [» Алгоритм зіставлення Unicode](http://www.unicode.org/reports/tr10/)
