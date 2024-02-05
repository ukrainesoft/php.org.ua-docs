---
navigation:
  - phar.apiversion.md: '« Phar::apiVersion'
  - phar.buildfromiterator.md: 'Phar::buildFromIterator »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::buildFromDirectory'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::buildFromDirectory

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::buildFromDirectory — Створює phar-архів із файлів, розташованих усередині директорії

### Опис

```methodsynopsis
public Phar::buildFromDirectory(string $directory, string $pattern = ""): array
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Заповнює phar-архів вмістом директорії. Необов'язковий другий параметр є регулярним виразом (PCRE) та використовується для виключення файлів. Будь-який файл, ім'я якого відповідає регулярному виразу, буде включений, всі інші будуть виключені. Для більш детального контролю використовуйте [Phar::buildFromIterator()](phar.buildfromiterator.md)

### Список параметрів

`directory`

Повний або абсолютний шлях до директорії, всі файли якої мають бути додані до архіву.

`pattern`

Необов'язковий регулярний вираз (PCRE), який використовується для фільтрації списку файлів. До архіву будуть включені лише ті файли, шляхи до яких відповідають регулярному виразу.

### Значення, що повертаються

**Phar::buildFromDirectory()** повертає асоціативний масив, в якому відображено відповідність шляху до файлу всередині архіву до шляху до файлу у файловій системі.

### Помилки

Цей метод викидає виняток [BadMethodCallException](class.badmethodcallexception.md) у разі, якщо не вдалося створити примірник ітератора внутрішніх директорій. Виняток [PharException](class.pharexception.md) викидається у разі помилок збереження phar-архіву.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | **Phar::buildFromDirectory()** більше не повертає значення **`false`** |

### Приклади

**Пример #1 Пример использования**Phar::buildFromDirectory()\*\*\*\*

```php
<?php
// создать с псевдонимом "project.phar"
$phar = new Phar('project.phar', 0, 'project.phar');
// добавить все файлы директории project в файл project.phar
$phar->buildFromDirectory(dirname(__FILE__) . '/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));

$phar2 = new Phar('project2.phar', 0, 'project2.phar');
// добавить все файлы директории project в файл project2.phar, включая только php-файлы
$phar2->buildFromDirectory(dirname(__FILE__) . '/project', '/\.php$/');
$phar2->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

### Дивіться також

-   [Phar::buildFromIterator()](phar.buildfromiterator.md) \- Створює phar-архів із ітератора
