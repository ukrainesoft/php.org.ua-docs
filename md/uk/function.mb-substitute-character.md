---
navigation:
  - function.mb-strwidth.md: « mb\_strwidth
  - function.mb-substr-count.md: mb\_substr\_count »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: mb\_substitute\_character
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mb\_substitute\_character

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

mb\_substitute\_character — Встановлює/отримує символ заміни

### Опис

```methodsynopsis
mb_substitute_character(string|int|null $substitute_character = null): string|int|bool
```

Задає заміщувальний символ на випадок, коли кодування вхідних даних неправильне або код символу не існує в кодуванні вихідних даних. Неприпустимі символи можуть бути замінені на `«none»` (немає виводу), рядок (string) чи числове значення (int) (код символу Юнікоду).

Ця установка впливає на поведінку таких функцій: [mb\_convert\_encoding()](function.mb-convert-encoding.md) [mb\_convert\_variables()](function.mb-convert-variables.md) [mb\_output\_handler()](function.mb-output-handler.md), и[mb\_send\_mail()](function.mb-send-mail.md)

### Список параметрів

`substitute_character`

Задає значення Юнікоду у вигляді цілого числа (int) або одного з наступних рядків string:

-   `«none»`: немає висновку
-   `«long»`: код кінцевого (у вихідному кодуванні) символу (Приклад:`U+3000` `JIS+7E7E`) .
-   `«entity»`: сутність кінцевого (у вихідному кодуванні) символу (Приклад:`&#x200;`) .

### Значення, що повертаються

Якщо аргумент `substitute_character` заданий, функція поверне **`true`** у разі успішного виконання, інакше **`false`**. Якщо символ `substitute_character` не встановлено, буде повернуто поточне налаштування.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Передача порожнього рядка до параметра `substitute_character` більше не підтримується; натомість необхідно передавати `«none»` |
| 8.0.0 | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Пример #1 Пример использования функции**mb\_substitute\_character()\*\*\*\*

```php
<?php
/* Установка замещающего символа Unicode U+3013 (GETA MARK) */
mb_substitute_character(0x3013);

/* Задаём шестнадцатеричный формат */
mb_substitute_character("long");

/* Отображение текущей настройки */
echo mb_substitute_character();
?>
```
