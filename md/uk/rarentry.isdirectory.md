- [« RarEntry::getVersion](rarentry.getversion.md)
- [RarEntry::isEncrypted »](rarentry.isencrypted.md)

- [PHP Manual](index.md)
- [RarEntry](class.rarentry.md)
- Перевіряє, чи є запис директорією

# RarEntry::isDirectory

(PECL rar \>= 2.0.0)

RarEntry::isDirectory — Перевіряє, чи є запис директорією

### Опис

public **RarEntry::isDirectory**(): bool

Перевіряє, чи є поточний запис директорією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** залежно від результату.

### Примітки

Функція доступна з версії 2.0.0, а для попередніх версій можна
перевіряти атрибути запису (Працює тільки для файлів, стиснутих у RAR для
Windows або Unix):

` <?php//...//Відкриємо файл, отримаємо запис і збережемо в змінною $e...//...$isDirectory = (bool) ((($e->getHostOs() ===RAR_HOST_WIN32) && ($e->getAttr() & 0x10)) ||    (($e->getHostOs() == RAR_HOST_UNIX) && (($e->getAttr()= 0xf000)); `
