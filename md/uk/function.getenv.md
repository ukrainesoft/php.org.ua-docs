---
navigation:
  - function.get-resources.md: « getresources
  - function.getlastmod.md: getlastmod »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getenv
---
# getenv

(PHP 4, PHP 5, PHP 7, PHP 8)

getenv — Отримання значення змінної оточення

### Опис

```methodsynopsis
getenv(string $varname, bool $local_only = false): string|false
```

```methodsynopsis
getenv(): array
```

Отримує значення змінного середовища.

Список усіх змінних оточення можна переглянути за допомогою функції [phpinfo()](function.phpinfo.md). Багато з цих змінних є у документі [» RFC 3875](http://www.faqs.org/rfcs/rfc3875), здебільшого у розділі 4.1, "Request Meta-Variables".

### Список параметрів

`varname`

Ім'я змінної.

`local_only`

Встановіть значення **`true`** для отримання лише локальних змінних оточення (встановлені операційною системою або командою putenv).

### Значення, що повертаються

Повертає значення змінного середовища `varname` або **`false`**, якщо змінною `varname` не існує. Якщо `varname` опущено, буде повернуто всі змінні оточення як асоціативного масиву (array).

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `varname` тепер може бути опущений для одержання асоціативного масиву (array) всіх змінних оточення. |
|  | Було додано параметр `local_only` |

### Приклади

**Приклад #1 Приклад використання **getenv()****

```php
<?php
// Пример использования getenv()
$ip = getenv('REMOTE_ADDR');

// Можно ещё воспользоваться суперглобальной переменной ($_SERVER или $_ENV)
$ip = $_SERVER['REMOTE_ADDR'];

// Гарантированно получаем значение переменной окружения, не обращая внимания,
// была ли она переопределена SAPI или изменена с помощью putenv
$ip = getenv('REMOTE_ADDR', true) ?: getenv('REMOTE_ADDR');
?>
```

### Примітки

**Увага**

Якщо PHP запущено в SAPI, наприклад, як Fast CGI, ця функція буде повертати значення змінних оточення встановлених SAPI, навіть якщо ви використовували [putenv()](function.putenv.md) для встановлення локальної змінної з таким самим ім'ям. Використовуйте параметр `local_only` для отримання встановлених локально змінних.

### Дивіться також

-   [putenv()](function.putenv.md) - Встановлює значення змінного середовища
-   [apachegetenv()](function.apache-getenv.md) - Повертає змінну оточення підпроцесу сервера Apache
-   [Суперглобальні змінні](language.variables.superglobals.md)
