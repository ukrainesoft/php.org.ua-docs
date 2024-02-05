---
navigation:
  - phar.buildfromdirectory.md: '« Phar::buildFromDirectory'
  - phar.cancompress.md: 'Phar::canCompress »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::buildFromIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::buildFromIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::buildFromIterator - Створює phar-архів з ітератора

### Опис

```methodsynopsis
public Phar::buildFromIterator(Traversable $iterator, ?string $baseDirectory = null): array
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Заповнює phar-архів із ітератора. Підтримуються ітератори двох типів: такі, де відображається відповідність імені файлу всередині phar-архіву до файлу на диску, і такі як DirectoryIterator, які повертають об'єкти SplFileInfo. Для ітераторів, які повертають об'єкти SplFileInfo, другий параметр є обов'язковим.

### Список параметрів

`iterator`

Будь-який ітератор, який або асоціативно відображає шляхи до файлів усередині phar-архіву до файлів на диску, або повертає об'єкти SplFileInfo.

`baseDirectory`

Для ітераторів, що повертають об'єкти SplFileInfo, - частина повного шляху кожного файлу, яка має бути видалена під час його додавання до phar-архіву.

### Значення, що повертаються

**Phar::buildFromIterator()** повертає асоціативний масив, у якому відображаються відповідності шляху до файлу всередині архіву до шляху до файлу у файловій системі.

### Помилки

Цей метод викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md)коли ітератор повертає некоректні значення, такі як цілий ключ замість рядка. Виняток [BadMethodCallException](class.badmethodcallexception.md) буде кинуто, коли ітератор, що базується на SplFileInfo, використовується без параметра `baseDirectory`Исключение[PharException](class.pharexception.md) викидається у разі помилок збереження phar-архіву.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | **Phar::buildFromIterator()** більше не повертає значення **`false`** |
| 8.0.0 | `baseDirectory` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** Phar::buildFromIterator()\*\* з об'єктами SplFileInfo\*\*

Для більшості phar-архівів, архів буде відображати фактичну структуру директорії, а другий тип ітератора буде найбільш корисним. Наприклад, він буде корисним для створення phar-архіву, що містить файли зі структурою директорій як у цьому прикладі:

/шлях/до/проекту/ config/ dist.xml debug.xml lib/ file1.php file2.php src/ processthing.php www/ index.php cli/ index.php

Для додавання цих файлів до phar-архів "project.phar" може бути використаний наступний код:

```php
<?php
// создать с псевдонимом "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new RecursiveDirectoryIterator('/путь/к/проекту')),
    '/путь/к/проекту');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

Після цього файл project.phar можна використовувати негайно. Такі значення як стиснення та метадані не встановлюються методом **Phar::buildFromIterator()** та можуть бути встановлені після створення phar-архіву.

Як цікаве зауваження можна відзначити, що **Phar::buildFromIterator()** також може бути використаний для копіювання вмісту існуючого phar-архіву, оскільки клас Phar є нащадком [DirectoryIterator](class.directoryiterator.md) :

```php
<?php
// создать с псевдонимом "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new Phar('/путь/к/anotherphar.phar')),
    'phar:///путь/к/anotherphar.phar/путь/к/проекту');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

**Приклад #2 Приклад використання** Phar::buildFromIterator()\*\* з іншими типами ітераторів\*\*

Другий тип передбачає використання будь-якого ітератора, що повертаються значення якого відображають відповідність імені файлу всередині phar-архіву до файлу на диску, як у випадку з [ArrayIterator](class.arrayiterator.md) :

```php
<?php
// создать с псевдонимом "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
$phar->buildFromIterator(
    new ArrayIterator(
     array(
        'путь/внутри/архива/file.php' => dirname(__FILE__) . '/somefile.php',
        'друго/путь/внутри/архива/file.jpg' => fopen('/путь/к/bigfile.jpg', 'rb'),
     )));
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

### Дивіться також

-   [Phar::buildFromDirectory()](phar.buildfromdirectory.md) \- Створює phar-архів із файлів, розташованих усередині директорії
