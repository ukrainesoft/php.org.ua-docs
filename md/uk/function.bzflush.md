- [«bzerrstr](function.bzerrstr.md)
- [bzopen »](function.bzopen.md)

- [PHP Manual](index.md)
- [Функції Bzip2](ref.bzip2.md)
-   Нічого не робить

# bzflush

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

bzflush - Нічого не робить

### Опис

**bzflush**(resource `$bz`): bool

Функція повинна примусово записувати всі буферизовані дані bzip2
у файл, який посилається покажчик `bz`, але у libbz2 реалізована як
нульова функція і тому нічого не робить.

### Список параметрів

`bz`
Вказівник на файл. Повинен бути коректним і вказувати на файл успішно
відкритий [bzopen()](function.bzopen.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Дивіться також

- [bzread()](function.bzread.md) - Бінарно-безпечне читання файлу
bzip2
- [bzwrite()](function.bzwrite.md) - Бінарно-безпечний запис bzip2
файлу
