- [« PharFileInfo::hasMetadata](pharfileinfo.hasmetadata.md)
- [PharFileInfo::isCompressed »](pharfileinfo.iscompressed.md)

- [PHP Manual](index.md)
- [PharFileInfo](class.pharfileinfo.md)
- Визначити, чи файл пройшов перевірку CRC

# PharFileInfo::isCRCChecked

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL phar = 1.0.0)

PharFileInfo::isCRCChecked — Визначити, чи пройшов файл перевірку CRC

### Опис

public **PharFileInfo::isCRCChecked**(): bool

Визначає, чи файл пройшов перевірку CRC.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо файл пройшов перевірку CRC, **`false`** у протилежному
випадку.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::isCRCChecked()****

`<?phptry {    $p = new Phar('/path/to/my.phar', 0, 'my.phar'); $p['myfile.txt'] = 'hi'; $file==$p['myfile.txt']; var_dump($file->isCRCChecked());} catch (Exception $e) {    echo 'Не удалося створити/змінити my.phar: ', $e;}?> `

Результат виконання цього прикладу:

bool(true)
