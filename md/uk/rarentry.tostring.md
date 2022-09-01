---
navigation:
  - rarentry.isencrypted.html: '« RarEntry::isEncrypted'
  - class.rarexception.html: RarException »
  - index.html: PHP Manual
  - class.rarentry.html: RarEntry
title: 'RarEntry::function toString() { \[native code\] }'
---
# RarEntry::function toString() { \[native code\] }

(PECL rar >= 2.0.0)

RarEntry::toString — Отримати текстове подання запису

### Опис

```methodsynopsis
public RarEntry::__toString(): string
```

**RarEntry::toString()** повертає текстове подання для поточного запису. Воно буде містити інформацію про те, чи є запис файлом або директорією (символічні посилання та інші спеціальні об'єкти будуть вважатися файлами), ім'я запису кодування UTF-8 та її контрольна сума (CRC). Вигляд і змістом цієї інформації в майбутньому може змінитися, так що не варто на них покладатися.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текстове подання запису.
