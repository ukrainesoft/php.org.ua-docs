---
navigation:
  - php-user-filter.onclose.html: '« phpuserfilter::onClose'
  - class.streamwrapper.md: streamWrapper »
  - index.md: PHP Manual
  - class.php-user-filter.html: phpuserfilter
title: 'phpuserfilter::onCreate'
---
# phpuserfilter::onCreate

(PHP 5, PHP 7, PHP 8)

phpuserfilter::onCreate — Викликається під час створення об'єкта фільтра

### Опис

```methodsynopsis
public php_user_filter::onCreate(): bool
```

Цей метод викликається під час створення фільтра під час створення екземпляра класу. У цьому вся методі можна виділяти необхідні ресурси та ініціалізувати об'єкти (наприклад, різні буфери).

Коли фільтр спочатку створюється та викликається метод `yourfilter->onCreate()`, буде доступний ряд таких властивостей, які описані в таблиці.

| Свойство | Содержание |
| --- | --- |
| `FilterClass->filtername` | Рядок, що містить ім'я фільтра, присвоєне йому під час створення. Фільтри можна реєструвати під різними іменами чи спецсимволами. Цю властивість можна використовувати визначення, яке ім'я було використано. |
| `FilterClass->params` | Вміст аргументу `params` передається у функцію [streamfilterappend()](function.stream-filter-append.html) або [streamfilterprepend()](function.stream-filter-prepend.md) |
| `FilterClass->stream` | Ресурс потоку, який фільтруватиметься. Властивість доступна, тільки якщо метод **filter()** викликається, коли параметр `closing` дорівнює **`false`** |

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ваша реалізація методу має повертати **`false`** при невдалому завершенні роботи або **`true`** при успішному.
