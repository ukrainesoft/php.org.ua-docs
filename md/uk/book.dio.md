---
navigation:
  - refs.fileprocess.file.md: « Модулі для роботи з файловою системою
  - intro.dio.md: Введение »
  - index.md: PHP Manual
  - refs.fileprocess.file.md: Модулі для роботи з файловою системою
title: Пряме введення/виведення (Direct IO)
---
# Пряме введення/виведення (Direct IO)

-   [Введение](intro.dio.md)
-   [Встановлення та налаштування](dio.setup.md)
    -   [Вимоги](dio.requirements.md)
    -   [Установка](dio.installation.md)
    -   [Налаштування під час виконання](dio.configuration.md)
    -   [Типи ресурсів](dio.resources.md)
-   [Обумовлені константи](dio.constants.md)
-   [Функції прямого введення/виводу](ref.dio.md)
    -   [dioclose](function.dio-close.md) - Закрити файловий дескриптор
    -   [diofcntl](function.dio-fcntl.md) — Викликає функцію бібліотеки C fcntl для файлового дескриптора
    -   [dioopen](function.dio-open.md) — Відкриває файл (за потребою створює) на нижчому рівні, ніж потокові функції введення/виведення мови C
    -   [dioread](function.dio-read.md) — Прочитай байти із файлового дескриптора
    -   [dioseek](function.dio-seek.md) — Перемістити вказівник у файловому дескрипторі
    -   [diostat](function.dio-stat.md) — Отримати інформацію про файловий дескриптор
    -   [diotcsetattr](function.dio-tcsetattr.md) — Встановлює атрибути терміналу та швидкість передачі даних для послідовного порту
    -   [diotruncate](function.dio-truncate.md) - Обрізає файл до заданої кількості байт
    -   [diowrite](function.dio-write.md) — Записує байти у файл, опціонально обрізаючи до вказаної довжини
