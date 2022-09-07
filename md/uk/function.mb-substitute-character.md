---
navigation:
  - function.mb-strwidth.md: « mbstrwidth
  - function.mb-substr-count.md: мбsubstrcount »
  - index.md: PHP Manual
  - ref.mbstring.md: Функції для роботи з багатобайтовими рядками
title: мбsubstitutecharacter
---
# мбsubstitutecharacter

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

мбsubstitutecharacter — Встановити/отримати символ заміни

### Опис

```methodsynopsis
mb_substitute_character(string|int|null $substitute_character = null): string|int|bool
```

Задає заміщувальний символ на випадок, коли кодування вхідних даних неправильне або код символу не існує в кодуванні вихідних даних. Неприпустимі символи можуть бути замінені на `"none"` (немає виводу), рядок (string) чи числове значення (int) (код символу Юнікоду).

Ця установка впливає на поведінку таких функцій: [мбconvertencoding()](function.mb-convert-encoding.md) [мбconvertvariables()](function.mb-convert-variables.md) [мбoutputhandler()](function.mb-output-handler.md), і [мбsendmail()](function.mb-send-mail.md)

### Список параметрів

`substitute_character`

Задає значення Юнікоду у вигляді числа (int) або одного з наступних рядків string:

-   `"none"` : немає висновку
-   `"long"` : код кінцевого (у вихідному кодуванні) символу (Приклад: `U+3000` `JIS+7E7E`
-   `"entity"` : сутність кінцевого (у вихідному кодуванні) символу (Приклад: `&#x200;`

### Значення, що повертаються

Якщо аргумент `substitute_character` заданий, функція поверне **`true`** у разі успішного виконання, **`false`** в іншому випадку. Якщо `substitute_character` не встановлено, буде повернуто поточне налаштування.

### список змін

| Версия | Описание |
| --- | --- |
|  | Передача порожнього рядка в `substitute_character` більше не підтримується; замість цього використовуйте `"none"` |
|  | Тепер параметр `encoding` може набувати значення **`null`** |

### Приклади

**Приклад #1 Приклад використання **мбsubstitutecharacter()****

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
