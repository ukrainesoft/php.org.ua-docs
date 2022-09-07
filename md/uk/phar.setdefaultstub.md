---
navigation:
  - phar.setalias.md: '« Phar::setAlias'
  - phar.setmetadata.md: 'Phar::setMetadata »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::setDefaultStub'
---
# Phar::setDefaultStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::setDefaultStub — Встановити завантажувач PHP або початкову заглушку Phar-архіву в завантажувач за замовчуванням

### Опис

```methodsynopsis
public Phar::setDefaultStub(?string $index = null, ?string $webIndex = null): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Цей метод комбінує функціональність двох інших методів, [Phar::createDefaultStub()](phar.createdefaultstub.md) і [Phar::setStub()](phar.setstub.md)

### Список параметрів

`index`

Відносний шлях у phar-архіві для запуску при доступі з командного рядка

`webIndex`

Відносний шлях у phar-архіві для запуску при доступі з веб-браузера

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Буде викинуто виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо [phar.readonly](phar.configuration.md#ini.phar.readonly) дозволено у php.ini. У разі проблем із записом на диск буде викинуто виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `webIndex` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::setDefaultStub()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setDefaultStub('cli.php', 'web/index.php');
    // это аналогично такому коду:
    // $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::setStub()](phar.setstub.md) - Встановити завантажувач або завантажувальну заглушку в Phar-архів
-   [Phar::createDefaultStub()](phar.createdefaultstub.md) - Створити заглушку у форматі phar-архіву
