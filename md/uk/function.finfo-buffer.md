- [« Функції модуля Fileinfo](ref.fileinfo.md)
- [finfo_close »](function.finfo-close.md)

- [PHP Manual](index.md)
- [Функції модуля Fileinfo](ref.fileinfo.md)
- Повертає інформацію про рядок буфера

#finfo_buffer

# finfo::buffer

(PHP 5 \>= 5.3.0, PHP 7, PHP 8, PECL fileinfo \>= 0.1.0)

finfo_buffer -- finfo::buffer — Повертає інформацію про рядок буфера

### Опис

Процедурний стиль

[finfo_buffer](finfo.buffer.md)(
[finfo](class.finfo.md) `$finfo`,
string `$string`,
int `$flags` = **`FILEINFO_NONE`**,
?resource `$context` = **`null`**
): string\|false

Об'єктно-орієнтований стиль

public [finfo::buffer](finfo.buffer.md)(string `$string`, int `$flags`
= **`FILEINFO_NONE`**, ?resource `$context` = **`null`**): string\|false

Ця функція використовується для отримання інформації про бінарних даних
рядку.

### Список параметрів

`finfo`
Примірник [finfo](class.finfo.md), що повертається функцією
[finfo_open()](function.finfo-open.md).

`string`
Вміст файлу, що перевіряється.

`flags`
Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.md).

`context`

### Значення, що повертаються

Повертає текстовий опис для аргументу `string` або **`false`**
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| 8.1.0  | Параметр finfo тепер чекає на екземпляр [finfo](class.finfo.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |
| 8.0.0  | 'context' тепер допускає значення null.                                                                                             |

### Приклади

**Приклад #1 Приклад [finfo_buffer()](finfo.buffer.md)**

` <?php$finfo = new finfo(FILEINFO_MIME);echo $finfo->buffer($_POST["script"]) . "
";?> `

Результатом виконання цього прикладу буде щось подібне:

application/x-sh; charset=us-ascii

### Дивіться також

- [finfo_file()](finfo.file.md) - Псевдонім finfo_file()
