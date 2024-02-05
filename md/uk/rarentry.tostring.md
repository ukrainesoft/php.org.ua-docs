---
navigation:
  - rarentry.isencrypted.md: '« RarEntry::isEncrypted'
  - class.rarexception.md: RarException »
  - index.md: PHP Manual
  - class.rarentry.md: RarEntry
title: 'RarEntry::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarEntry::\_\_function toString() { \[native code\] }

(PECL rar >= 2.0.0)

RarEntry::\_\_toString — Отримати текстове подання запису

### Опис

```methodsynopsis
public RarEntry::__toString(): string
```

**RarEntry::\_\_toString()** повертає текстове подання для поточного запису. Воно міститиме інформацію про те, чи є запис файлом або директорією (символічні посилання та інші спеціальні об'єкти будуть вважатися файлами), ім'я запису в кодуванні UTF-8 та її контрольна сума (CRC). Вигляд та зміст цієї інформації в майбутньому може змінитися, так що не варто на них покладатися.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текстове подання запису.
