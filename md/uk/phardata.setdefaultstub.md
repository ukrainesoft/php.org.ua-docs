---
navigation:
  - phardata.setalias.md: '« PharData::setAlias'
  - phardata.setmetadata.md: 'PharData::setMetadata »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::setDefaultStub'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::setDefaultStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::setDefaultStub — Функція заглушку (Phar::setDefaultStub не можна використовувати для PharData)

### Опис

```methodsynopsis
public PharData::setDefaultStub(?string $index = null, ?string $webIndex = null): bool
```

tar/zip-архіви, що не запускаються, не можуть мати заглушку, так що цей метод просто викидає виняток.

### Список параметрів

`index`

Відносний шлях у phar-архіві для запуску при доступі з командного рядка

`webIndex`

Відносний шлях у phar-архіві для запуску при доступі через браузер

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає виняток [PharException](class.pharexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `webIndex` тепер допускає значення null. |

### Дивіться також

-   [Phar::setDefaultStub()](phar.setdefaultstub.md) \- Встановити завантажувач PHP або початкову заглушку Phar-архіву в завантажувач за замовчуванням
