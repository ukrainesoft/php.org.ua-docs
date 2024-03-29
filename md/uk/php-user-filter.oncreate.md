---
navigation:
  - php-user-filter.onclose.md: '« php\_user\_filter::onClose'
  - class.streamwrapper.md: streamWrapper »
  - index.md: PHP Manual
  - class.php-user-filter.md: php\_user\_filter
title: 'php\_user\_filter::onCreate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# php\_user\_filter::onCreate

(PHP 5, PHP 7, PHP 8)

php\_user\_filter::onCreate — Викликається під час створення об'єкта фільтра

### Опис

```methodsynopsis
public php_user_filter::onCreate(): bool
```

Цей метод викликається під час створення фільтра під час створення екземпляра класу. У цьому методі можна виділяти необхідні ресурси та ініціалізувати об'єкти (наприклад, різні буфери).

Коли фільтр спочатку створюється та викликається метод `yourfilter->onCreate()`, буде доступний ряд таких властивостей, які описані в таблиці.

| Свойство | Содержание |
| --- | --- |
| `FilterClass->filtername` | Рядок, що містить ім'я фільтра, присвоєне йому під час створення. Фільтри можна реєструвати під різними іменами чи спецсимволами. Цю властивість можна використовувати визначення, яке ім'я було використано. |
| `FilterClass->params` | Вміст аргументу `params` передається у функцію [stream\_filter\_append()](function.stream-filter-append.md) або [stream\_filter\_prepend()](function.stream-filter-prepend.md) |
| `FilterClass->stream` | Ресурс потоку, який фільтруватиметься. Властивість доступна, тільки якщо метод **filter()** викликається, коли параметр `closing`равен\*\*`false`\*\* |

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ваша реализация метода должна возвращать\*\*`false`\*\* при невдалому завершенні роботи або **`true`** при успішному.
