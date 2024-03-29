---
navigation:
  - outcontrol.constants.md: « Зумовлені константи
  - outcontrol.flushing-system-buffers.md: Скидання (відправлення) системних буферів »
  - index.md: PHP Manual
  - book.outcontrol.md: Контроль виведення
title: Буферизація висновку
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Буферизація висновку

Буферизація виводу — це буферизація, або тимчасове зберігання, виводу перед скиданням, тобто перед відправкою та видаленням, у браузер у веб-контексті або командну оболонку в командному рядку. Поки буферизація виводу активна, виведення зі скрипту не відправляється, натомість висновок зберігається у внутрішньому буфері.

## Буферизація, що впливає на PHP

PHP спирається на базову програмно-апаратну інфраструктуру під час скидання висновку. Буферизація, яка реалізована консолями в командному рядку (наприклад, з буферизацією рядка) або веб-серверами та браузером у веб-контексті (наприклад, з повною буферизацією), впливає на те, коли виведення відображається кінцевому користувачеві. Частина цих ефектів вдасться усунути тонким налаштуванням параметрів сервера та (або) вирівнюванням розмірів буферів на різних рівнях.

## Контроль буферизації виведення в PHP

Розробники PHP передбачили повністю буферизований користувальницький буфер виведення з функціями для запуску, маніпулювання та відключення буфера (більша частина [ob\_\*](ref.outcontrol.md)\-функцій), та дві функції для скидання базових системних буферів (функції [flush()](function.flush.md) і [ob\_implicit\_flush()](function.ob-implicit-flush.md)). Частина цієї функціональності також встановлюють та (або) конфігурують у налаштуваннях файлу php.ini.

## Коли корисна буферизація

Буферизація висновку корисна у ситуаціях, у яких буферизований висновок змінюється чи перевіряється, або його перевикористовують у запиті; або коли потрібне контрольоване очищення вихідних даних. Конкретні сценарії роботи з буферами включають:

-   кешування результатів виконання скриптів, що вимагають складних обчислень або часу, наприклад, при генерації статичних`HTML`\-сторінок
-   перевикористання згенерованого виводу шляхом його відображення, збереження у файл та (або) відправки електронною поштою
-   скидання заголовка (`head` `HTML`\-сторінки до відправлення тіла (`body`), щоб дозволити браузерам завантажувати зовнішні ресурси, поки скрипт вирішує завдання, здатні забрати більше часу (наприклад, отримує доступ до бази даних або файлу, встановлює зовнішнє мережне підключення). Це корисно лише тоді, коли`HTTP`\-код стану не можна змінити після надсилання заголовків
-   вилучення інформації з функцій, які інакше видавали б висновок (наприклад, функція[phpinfo()](function.phpinfo.md)) .
-   керування виведенням стороннього коду шляхом зміни або включення його частин (наприклад, вилучення даних, заміна слів або фраз, додавання відсутніх)`HTML`\-тегів) або повної відмови від цього коду за конкретних умов (наприклад, при помилках)
-   поліфілінг недоступної функціональності веб-сервера (наприклад, стиснення або кодування виводу)
