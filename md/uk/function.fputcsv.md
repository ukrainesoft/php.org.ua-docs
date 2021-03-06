- [«fpassthru](function.fpassthru.md)
- [fputs »](function.fputs.md)

- [PHP Manual](index.md)
- [Функції файлової системи](ref.filesystem.md)
- Форматує рядок у вигляді CSV та записує її у файловий покажчик

# fputcsv

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

fputcsv — Форматує рядок у вигляді CSV та записує його у файловий
покажчик

### Опис

**fputcsv**(
resource `$stream`,
array `$fields`,
string `$separator` = ",",
string `$enclosure` = "\"",
string `$escape` = "\\",
string `$eol` = "
"
): int\|false

**fputcsv()** форматує рядок (переданий у вигляді масиву `fields`) в
CSV і записує її (закінчуючи перекладом рядка) у вказаний файл
`stream`.

### Список параметрів

`stream`
Вказівник на файл повинен бути коректним і вказувати на файл успішно
відкритий функціями [fopen()](function.fopen.md) або
[fsockopen()](function.fsockopen.md) (і все ще не закритий функцією
[fclose()](function.fclose.md)).

`fields`
Масив рядків (string).

`separator`
Додатковий параметр `separator` встановлює роздільник полів
(лише один однобайтовий символ).

`enclosure`
Додатковий параметр `enclosure` встановлює обмежувач полів
(лише один однобайтовий символ).

`escape`
Необов'язковий параметр `escape` задає екрануючий символ (не більше
одного однобайтового символу). Порожній рядок (`````) відключає
пропрієтарний механізм екранування.

`eol`
Необов'язковий параметр `eol` задає послідовність, що настроюється.
кінця рядка.

> **Примітка**:
>
> Якщо символ "enclosure" міститься в полі, він буде екрановано шляхом
> його подвоєння, якщо йому передує `escape`.

### Значення, що повертаються

Повертає довжину записаного рядка або **`false`** у разі
виникнення помилки.

### Список змін

| Версія | Опис                                                                                                     |
|--------|----------------------------------------------------------------------------------------------------------|
| 8.1.0  | Додано необов'язковий параметр eol.                                                                      |
| 7.4.0  | Тепер параметр escape може приймати порожній рядок для відключення пропрієтарного механізму екранування. |

### Приклади

**Приклад #1 Приклад використання **fputcsv()****

` <?php$list = array (    array('aaa', 'bbb', ccc', dddd'),   array('123', '456', '789'),   , '"bbb"'));$fp =fopen('file.csv', 'w');foreach ($list as $fields) {   fputcsv($fp, $fields);}fclose($fp); ?> `

Наведений вище приклад запише в файл `file.csv` наступне:

aaa, bbb, ccc, dddd
123,456,789
"""aaa""","""bbb"""

### Примітки

> **Примітка**: Якщо у вас виникають проблеми з розпізнаванням PHP
> кінців рядків під час читання або створення файлів на Macintosh-сумісному
> комп'ютер, включення опції
> [auto_detect_line_endings](filesystem.configuration.md#ini.auto-detect-line-endings)
> допоможе вирішити проблему.

### Дивіться також

- [fgetcsv()](function.fgetcsv.md) - Читає рядок з файлу та
проводить розбір даних CSV
