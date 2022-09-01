---
navigation:
  - refs.fileprocess.file.html: « Модулі для роботи з файловою системою
  - intro.dio.html: Введение »
  - index.html: PHP Manual
  - refs.fileprocess.file.html: Модулі для роботи з файловою системою
title: Пряме введення/виведення (Direct IO)
---
# Пряме введення/виведення (Direct IO)

-   [Введение](intro.dio.html)
-   [Встановлення та налаштування](dio.setup.html)
    -   [Вимоги](dio.requirements.html)
    -   [Установка](dio.installation.html)
    -   [Налаштування під час виконання](dio.configuration.html)
    -   [Типи ресурсів](dio.resources.html)
-   [Обумовлені константи](dio.constants.html)
-   [Функції прямого введення/виводу](ref.dio.html)
    -   [dioclose](function.dio-close.html) - Закрити файловий дескриптор
    -   [diofcntl](function.dio-fcntl.html) — Викликає функцію бібліотеки C fcntl для файлового дескриптора
    -   [dioopen](function.dio-open.html) — Відкриває файл (за потребою створює) на нижчому рівні, ніж потокові функції введення/виведення мови C
    -   [dioread](function.dio-read.html) — Прочитай байти із файлового дескриптора
    -   [dioseek](function.dio-seek.html) — Перемістити вказівник у файловому дескрипторі
    -   [diostat](function.dio-stat.html) — Отримати інформацію про файловий дескриптор
    -   [diotcsetattr](function.dio-tcsetattr.html) — Встановлює атрибути терміналу та швидкість передачі даних для послідовного порту
    -   [diotruncate](function.dio-truncate.html) - Обрізає файл до заданої кількості байт
    -   [diowrite](function.dio-write.html) — Записує байти у файл, опціонально обрізаючи до вказаної довжини
