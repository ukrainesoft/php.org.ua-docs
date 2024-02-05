---
navigation:
  - phar.running.md: '« Phar::running'
  - phar.setdefaultstub.md: 'Phar::setDefaultStub »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::setAlias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::setAlias

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.1)

Phar::setAlias ​​— Встановити псевдонім для Phar-архіву

### Опис

```methodsynopsis
public Phar::setAlias(string $alias): bool
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Встановлює псевдонім для Phar-архіву та записує його як постійний псевдонім для цього архіву. Псевдонім можна використовувати всередині phar-архіву для впевненості в тому, що доступ через потокову обгортку `phar` для доступу до внутрішніх файлів буде працювати завжди, незалежно від розташування phar-архіву на файловій системі. Іншою альтернативою є надія на перехоплення [include](function.include.md)или использование[Phar::interceptFileFuncs()](phar.interceptfilefuncs.md) разом із відносними шляхами.

### Список параметрів

`alias`

Коротке ім'я, яке можна використовувати з доступом через потокову обгортку `phar`

### Значення, що повертаються

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо доступ заборонено та [PharException](class.pharexception.md)якщо псевдонім вже використовується, або виникли проблеми із записом на диск.

### Приклади

**Пример #1 Пример использования**Phar::setAlias()\*\*\*\*

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setAlias('myp.phar');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::\_\_construct()](phar.construct.md) \- Створює об'єкт Phar-архіву
-   [Phar::interceptFileFuncs()](phar.interceptfilefuncs.md) \- Вказує phar перехоплювати fopen, file\_get\_contents, opendir та всі stat-функції
