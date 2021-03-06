- [« dbase_delete_record](function.dbase-delete-record.md)
- [dbase_get_record_with_names »](function.dbase-get-record-with-names.md)

- [PHP Manual](index.md)
- [dBase](ref.dbase.md)
- Отримує інформацію про властивості полів бази даних

#dbase_get_header_info

(PHP 5 \< 5.3.0, dbase 5, dbase 7)

dbase_get_header_info — Отримує інформацію про властивості полів бази
даних

### Опис

**dbase_get_header_info**(resource `$database`): array

Повертає інформацію про структуру полів (стовпців) даного ресурсу бази
даних.

### Список параметрів

`database`
Ресурс бази даних, отриманий за допомогою
[dbase_open()](function.dbase-open.md) або
[dbase_create()](function.dbase-create.md).

### Значення, що повертаються

Індексований масив значень кожної колонки (поля). Індекс
масиву починається з 0.

Кожен елемент масиву містить асоціативний масив інформації про
стовпцях БД такого виду:

name
Найменування поля

type
Тип поля dBase у зручному для сприйняття вигляді (date, boolean, і т.д.)
Типи файлів, що підтримуються, перераховані у [вступний секції](intro.dbase.md).

length
Максимальна кількість байт даного поля, що зберігається (включаючи "precision" -
прим. пров.)

precision
Кількість цифр після коми

format
Запропонований в [printf()](function.printf.md) формат специфікації для
даного типу

offset
Байт усунення, що вказує розміщення поля від початку запису (рядки).

Якщо інформація в заголовку бази даних не може бути прочитана,
повертає **`false`**.

### Список змін

| Версія    | Опис                                                |
|-----------|-----------------------------------------------------|
| dbase 7.0 | Параметр database тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Отримання властивостей полів файлу бази даних dBase**

` <?php//Шлях до файлу БД$db_path = "/tmp/test.dbf";// Відкриваємо файл БД$dbh = dbase_open($db_path, 0) ід   '.");// Отримуємо інформацію про стовпці$column_info = dbase_get_header_info($dbh);// Відображення інформаціїprint_r($column_info);?> `
