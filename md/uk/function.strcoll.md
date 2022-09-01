---
navigation:
  - function.strcmp.md: « strcmp
  - function.strcspn.md: strcspn »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strcoll
---
# strcoll

(PHP 4> = 4.0.5, PHP 5, PHP 7, PHP 8)

strcoll — Порівняння рядків з урахуванням поточної локалі

### Опис

```methodsynopsis
strcoll(string $string1, string $string2): int
```

Зверніть увагу, що ця функція враховує регістр символів, і на відміну від [strcmp()](function.strcmp.md), не безпечна для обробки даних у двійковій формі.

**strcoll()** при порівнянні використовує установки поточної локалі. Якщо встановлено локаль C або POSIX, ця функція аналогічна [strcmp()](function.strcmp.md)

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Повертає негативне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо вони рівні.

### Дивіться також

-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [strcmp()](function.strcmp.md) - Бінарно-безпечне порівняння рядків
-   [strcasecmp()](function.strcasecmp.md) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.md) - Повертає підрядок
-   [stristr()](function.stristr.md) - Реєстронезалежний варіант функції strstr
-   [strncasecmp()](function.strncasecmp.md) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strncmp()](function.strncmp.md) - Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.md) - Знаходить перше входження підрядка
-   [setlocale()](function.setlocale.md) - Встановлює налаштування локалі
