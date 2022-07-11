- [« Transliterator::getErrorMessage](transliterator.geterrormessage.md)
- [Transliterator::transliterate »](transliterator.transliterate.md)

- [PHP Manual](index.md)
- [Transliterator](class.transliterator.md)
- Отримати ідентифікатори транслітератора

# Transliterator::listIDs

# transliterator_list_ids

(PHP 5 = 5.4.0, PHP 7, PHP 8, PECL intl = 2.0.0)

Transliterator::listIDs -- transliterator_list_ids — Отримати
ідентифікатори транслітератора

### Опис

Об'єктно-орієнтований стиль

public static **Transliterator::listIDs**(): array\|false

Процедурний стиль

**transliterator_list_ids**(): array\|false

Повертає масив зареєстрованих ідентифікаторів транслітератора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) зареєстрованих ідентифікаторів транслітератора або
**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання зареєстрованих ідентифікаторів
транслітератора**

` <?phpprint_r(Transliterator::listIDs());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => ASCII-Latin
[1] => Accents-Any
[2] => Amharic-Latin/BGN
[3] => Any-Accents
[4] => Any-Publishing
...
[650] => Any-ps_Latn/BGN
[651] => Any-tk/BGN
[652] => Any-ch_FONIPA
[653] => Any-cs_FONIPA
[654] => Any-cy_FONIPA
)

### Дивіться також

- [Transliterator::getErrorMessage()](transliterator.geterrormessage.md) -
Отримати останнє повідомлення про помилку
- [Transliterator::transliterate()](transliterator.transliterate.md) -
Транслітерувати рядок
