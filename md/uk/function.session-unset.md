---
navigation:
  - function.session-status.md: « session\_status
  - function.session-write-close.md: session\_write\_close »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_unset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_unset

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_unset — Видалити всі змінні сесії

### Опис

```methodsynopsis
session_unset(): bool
```

Функция**session\_unset()** видаляє всі зареєстровані змінні поточної сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Примітки

> **Зауваження** :
> 
> При использовании[$\_SESSION](reserved.variables.session.md) для видалення змінних сесії, то використовуйте функцію [unset()](function.unset.md)НаПриклад,`unset($_SESSION['varname']);`

**Застереження**

НЕ видаляйте весь масив [$\_SESSION](reserved.variables.session.md) за допомогою `unset($_SESSION)`, оскільки це призведе до неможливості реєстрації нових змінних через суперглобальний масив. [$\_SESSION](reserved.variables.session.md)

> **Зауваження** :
> 
> Использование функции**session\_unset()** ідентично `$_SESSION = []`

**Застереження**

Функція працює лише у випадку, якщо сесія активна. Вона не очистить масив [$\_SESSION](reserved.variables.session.md)якщо сесія ще не запущена або вже знищена. Використовуйте `$_SESSION = []` для видалення всіх змінних сесії навіть якщо сесія не активна.
