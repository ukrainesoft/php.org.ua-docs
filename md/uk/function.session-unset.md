Видалити всі змінні сесії

-   [« sessionstatus](function.session-status.html)
    
-   [sessionwriteclose »](function.session-write-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи із сесіями](ref.session.html)
    
-   Видалити всі змінні сесії
    

# sessionunset

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionunset — Видалити всі змінні сесії

### Опис

```methodsynopsis
session_unset(): bool
```

Функція **sessionunset()** видаляє всі зареєстровані змінні поточної сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Примітки

> **Зауваження**
> 
> При використанні [SESSION](reserved.variables.session.html) для видалення змінних сесії, то використовуйте функцію [unset()](function.unset.html). Наприклад, `unset ($_SESSION['varname']);`

**Застереження**

НЕ видаляйте весь масив [SESSION](reserved.variables.session.html) за допомогою `unset($_SESSION)`, оскільки це призведе до неможливості реєстрації нових змінних через суперглобальний масив. [SESSION](reserved.variables.session.html)

> **Зауваження**
> 
> Використовуйте **sessionunset()** тільки для старого коду, який не використовує [SESSION](reserved.variables.session.html)