- [« yaz_set_option](function.yaz-set-option.md)
- [yaz_syntax »](function.yaz-syntax.md)

- [PHP Manual](index.md)
- [Функції YAZ](ref.yaz.md)
- Задає критерій сортування

# yaz_sort

(PHP 4 = 4.0.7, PECL yaz = 0.9.0)

yaz_sort — Задає критерій сортування

### Опис

**yaz_sort**(resource `$id`, string `$criteria`): void

Функція визначає критерій сортування і включає сортування за Z39.50.

Ця функція має бути викликана *до*
[yaz_search()](function.yaz-search.md). Виклик цієї функції окремо не
не має сенсу. Коли вона використовується спільно з
[yaz_search()](function.yaz-search.md), параметри сортування будуть
надіслано після пошукового запиту і до того, як будь-який запис буде
отримана за Z39.50 ([yaz_present()](function.yaz-present.md)).

### Список параметрів

`id`
Дескриптор з'єднання, що повертається
[yaz_connect()](function.yaz-connect.md).

`criteria`
Рядок, що набуває вигляду поле1 прапор1 поле2 прапор2, де поле1 встановлює
перший атрибут сортування, поле2 – другий і т.д.

Поле може визначатися або як числова комбінація, що складається з пари
тип = значення і розділяється комою (наприклад, `1=4,2=1`), або як
рядковий параметр (наприклад, `title`). Прапор є
послідовність символів, яка може бути розділена пробілом.

`a`
Сортування за зростанням

`d`
Сортування за спаданням

`i`
Сортування без урахування регістру символів

`s`
Сортування з урахуванням регістру символів

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Критерії сортування**

Щоб відсортувати записи за заголовком, без урахування регістру за
зростанню слід використовувати наступний критерій:

``` examplescode
1=4 ia
````

Якщо другий критерій сортування повинен йти за автором з урахуванням регістру
і за зростанням, критерій виглядатиме як:

``` examplescode
1=4 ia 1=1003 sa
````
