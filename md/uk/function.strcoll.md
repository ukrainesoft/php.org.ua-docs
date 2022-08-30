Порівняння рядків з урахуванням поточної локалі

-   [« strcmp](function.strcmp.html)
    
-   [strcspn »](function.strcspn.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Порівняння рядків з урахуванням поточної локалі
    

# strcoll

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

strcoll — Порівняння рядків з урахуванням поточної локалі

### Опис

```methodsynopsis
strcoll(string $string1, string $string2): int
```

Зверніть увагу, що ця функція враховує регістр символів, і на відміну від [strcmp()](function.strcmp.html), не безпечна для обробки даних у двійковій формі.

**strcoll()** при порівнянні використовує установки поточної локалі. Якщо встановлено локаль C або POSIX, ця функція аналогічна [strcmp()](function.strcmp.html)

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Повертає негативне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо вони рівні.

### Дивіться також

-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [strcmp()](function.strcmp.html) - Бінарно-безпечне порівняння рядків
-   [strcasecmp()](function.strcasecmp.html) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.html) - Повертає підрядок
-   [stristr()](function.stristr.html) - Реєстронезалежний варіант функції strstr
-   [strncasecmp()](function.strncasecmp.html) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.html) - Знаходить перше входження підрядка
-   [setlocale()](function.setlocale.html) - Встановлює налаштування локалі