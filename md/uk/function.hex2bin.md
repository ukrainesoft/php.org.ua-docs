- [«hebrevc](function.hebrevc.md)
- [html_entity_decode »](function.md-entity-decode.md)

- [PHP Manual](index.md)
- [Функції для роботи з рядками](ref.strings.md)
- Перетворює шістнадцяткові дані на двійкові

# hex2bin

(PHP 5 \>= 5.4.0, PHP 7, PHP 8)

hex2bin — Перетворює шістнадцяткові дані на двійкові

### Опис

**hex2bin**(string `$string`): string\|false

Декодує рядок даних із шістнадцяткового подання.

**Застереження**

Ця функція *НЕ* конвертує шістнадцяткові числа на двійкові. Якщо
потрібно саме це, використовуйте функцію
[base_convert()](function.base-convert.md).

### Список параметрів

`string`
Шістнадцяткове представлення даних.

### Значення, що повертаються

Повертає двійкове подання даних або **`false`** у разі
виникнення помилки.

### Помилки

Якщо у вхідному шістнадцятковому рядку виявиться непарна кількість байт
або вона не є правильним шістнадцятковим рядком, буде видано
попередження **`E_WARNING`**.

### Приклади

**Приклад #1 Приклад використання **hex2bin()****

` <?php$hex = hex2bin("d0bfd180d0b8d0bcd0b5d18020d188d0b5d181d182d0bdd0b0d0b4d186d0b0d182d0b5d180d0b8d187d0bdd18bd18520d0b4d0b0d0bdd0bdd18bd185");var_dump($hex);?> `

Результатом виконання цього прикладу буде щось подібне:

string(60) "приклад шістнадцяткових даних"

### Дивіться також

- [bin2hex()](function.bin2hex.md) - Перетворює бінарні дані на
шістнадцяткове уявлення
- [unpack()](function.unpack.md) - Розпакувати дані з бінарної
рядки
