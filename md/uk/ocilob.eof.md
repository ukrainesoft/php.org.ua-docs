---
navigation:
  - ocilob.close.md: '« OCILob::close'
  - ocilob.erase.md: 'OCILob::erase »'
  - index.md: PHP Manual
  - class.ocilob.md: OCILob
title: 'OCILob::eof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OCILob::eof

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

OCILob::eof — Перевіряє, чи вказівник LOB знаходиться на кінці об'єкта.

### Опис

```methodsynopsis
public OCILob::eof(): bool
```

Повідомляє про досягнення внутрішнім покажчиком кінця об'єкта LOB.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо внутрішній покажчик об'єкта знаходиться на кінці LOB. Інакше повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Класс**OCI-Lob**перейменований на[OCILob](class.ocilob.md) відповідно до стандартів іменування PHP. |

### Примітки

> **Зауваження** :
> 
> Функція повертає Oracle помилку у разі, якщо [OCILob::setBuffering](ocilob.setbuffering.md)включена для LOB.

### Дивіться також

-   [OCILob::size](ocilob.size.md)
