---
navigation:
  - phar.setalias.html: '« Phar::setAlias'
  - phar.setmetadata.html: 'Phar::setMetadata »'
  - index.html: PHP Manual
  - class.phar.html: Phar
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
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Цей метод комбінує функціональність двох інших методів, [Phar::createDefaultStub()](phar.createdefaultstub.html) і [Phar::setStub()](phar.setstub.html)

### Список параметрів

`index`

Відносний шлях у phar-архіві для запуску при доступі з командного рядка

`webIndex`

Відносний шлях у phar-архіві для запуску при доступі з веб-браузера

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Буде викинуто виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо [phar.readonly](phar.configuration.html#ini.phar.readonly) дозволено у php.ini. У разі проблем із записом на диск буде викинуто виняток [PharException](class.pharexception.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | `webIndex` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::setDefaultStub()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setDefaultStub('cli.php', 'web/index.php');
    // это аналогично такому коду:
    // $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::setStub()](phar.setstub.html) - Встановити завантажувач або завантажувальну заглушку в Phar-архів
-   [Phar::createDefaultStub()](phar.createdefaultstub.html) - Створити заглушку у форматі phar-архіву
