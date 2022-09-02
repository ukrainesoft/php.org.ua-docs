---
navigation:
  - phardata.setalias.md: '« PharData::setAlias'
  - phardata.setmetadata.md: 'PharData::setMetadata »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::setDefaultStub'
---
# PharData::setDefaultStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::setDefaultStub — Функція заглушка (Phar::setDefaultStub не можна використовувати для PharData)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `webIndex` тепер допускає значення null. |

### Дивіться також

-   [Phar::setDefaultStub()](phar.setdefaultstub.md) - Встановити завантажувач PHP або початкову заглушку Phar-архіву в завантажувач за замовчуванням
