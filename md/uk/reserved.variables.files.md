---
navigation:
  - reserved.variables.post.md: « $\_POST
  - reserved.variables.request.md: $\_REQUEST »
  - index.md: PHP Manual
  - reserved.variables.md: Зумовлені змінні
title: $\_FILES
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# $\_FILES

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_FILES — Змінні файли, завантажені за HTTP

### Опис

Асоціативний масив (array) елементів, завантажених у поточний скрипт через метод HTTP POST. Структура цього масиву описана у розділі [Завантаження файлів методом POST](features.file-upload.post-method.md)

### Примітки

> **Зауваження** :
> 
> Це «суперглобальна» чи автоматична глобальна змінна. Це просто означає, що вона доступна у всіх контекстах скрипту. Немає необхідності виконувати **global $variable;** для доступу до неї всередині методу чи функції.

### Дивіться також

-   [move\_uploaded\_file()](function.move-uploaded-file.md) \- Переміщує завантажений файл у нове місце
-   [Завантаження файлів на сервер](features.file-upload.md)
