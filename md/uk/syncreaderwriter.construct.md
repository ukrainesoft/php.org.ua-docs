Створює новий об'єкт SyncReaderWriter

-   [« SyncReaderWriter](class.syncreaderwriter.md)
    
-   [SyncReaderWriter::readlock »](syncreaderwriter.readlock.md)
    
-   [PHP Manual](index.md)
    
-   [SyncReaderWriter](class.syncreaderwriter.md)
    
-   Створює новий об'єкт SyncReaderWriter
    

# SyncReaderWriter::construct

(PECL sync >= 1.0.0)

SyncReaderWriter::construct — Створює новий об'єкт SyncReaderWriter

### Опис

```methodsynopsis
public SyncReaderWriter::__construct(string $name = ?, int $autounlock = 1)
```

Створює іменований чи безіменний об'єкт читання-запису.

### Список параметрів

`name`

Ім'я засобу читання-запису, якщо це іменований об'єкт читання-запису.

> **Зауваження**
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

> **Зауваження**: У Windows параметр `name` не повинен містити зворотних слішів.

`autounlock`

Вказує, чи слід автоматично розблокувати засіб читання-запису під час завершення скрипту PHP.

**Увага**

Якщо об'єкт: Іменований засіб читання-запису з автоматичним блокуванням FALSE, об'єкт заблокований для читання або запису, і скрипт PHP завершується до того, як об'єкт буде розблокований, тоді базові об'єкти виявляться у неузгодженому стані.

### Значення, що повертаються

Новий об'єкт [SyncReaderWriter](class.syncreaderwriter.md)

### Помилки

Виняток викидається, якщо засіб читання-запису не може бути створений або відкритий.

### Приклади

**Приклад #1 Приклад використання **SyncReaderWriter::construct()****

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->readlock();
/* ... */
$readwrite->readunlock();

$readwrite->writelock();
/* ... */
$readwrite->writeunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::readlock()](syncreaderwriter.readlock.md) - Чекає на блокування читання
-   [SyncReaderWriter::readunlock()](syncreaderwriter.readunlock.md) - Знімає блокування читання
-   [SyncReaderWriter::writelock()](syncreaderwriter.writelock.md) - Чекає на ексклюзивне блокування запису
-   [SyncReaderWriter::writeunlock()](syncreaderwriter.writeunlock.md) - Знімає блокування запису