---
navigation:
  - refs.fileprocess.file.md: « Модулі для роботи з файловою системою
  - intro.dio.md: Вступ "
  - index.md: PHP Manual
  - refs.fileprocess.file.md: Модулі для роботи з файловою системою
title: Пряме введення/виведення (Direct IO)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Пряме введення/виведення (Direct IO)

-   [Вступ](intro.dio.md)
-   [Встановлення та налаштування](dio.setup.md)
    -   [Вимоги](dio.requirements.md)
    -   [Установка](dio.installation.md)
    -   [Налаштування під час виконання](dio.configuration.md)
    -   [Типи ресурсів](dio.resources.md)
-   [Обумовлені константи](dio.constants.md)
-   [Функції прямого введення/виводу](ref.dio.md)
    -   [dio\_close](function.dio-close.md) \- Закрити файловий дескриптор
    -   [dio\_fcntl](function.dio-fcntl.md)— Викликає функцію бібліотеки C fcntl для файлового дескриптора
    -   [dio\_open](function.dio-open.md)— Відкриває файл (за потребою створює) на нижчому рівні, ніж потокові функції введення/виведення мови C
    -   [dio\_read](function.dio-read.md)— Прочитай байти із файлового дескриптора
    -   [dio\_seek](function.dio-seek.md)— Перемістити вказівник у файловому дескрипторі
    -   [dio\_stat](function.dio-stat.md)— Отримати інформацію про файловий дескриптор
    -   [dio\_tcsetattr](function.dio-tcsetattr.md)— Встановлює атрибути терміналу та швидкість передачі даних для послідовного порту
    -   [dio\_truncate](function.dio-truncate.md) \- Обрізає файл до заданої кількості байт
    -   [dio\_write](function.dio-write.md)— Записує байти у файл, опціонально обрізуючи до вказаної довжини
