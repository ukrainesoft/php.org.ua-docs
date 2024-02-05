---
navigation:
  - splfileobject.fgetss.md: '« SplFileObject::fgetss'
  - splfileobject.fpassthru.md: 'SplFileObject::fpassthru »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::flock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::flock

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::flock — Портоване блокування файлу

### Опис

```methodsynopsis
public SplFileObject::flock(int $operation, int &$wouldBlock = null): bool
```

Блокує або розблокує файл тим же портованим способом, що і [flock()](function.flock.md)

### Список параметрів

`operation`

`operation` може приймати такі значення:

-   \*\*`LOCK_SH`\*\*для отримання блокування, що розділяється (читання).
-   \*\*`LOCK_EX`\*\*для отримання ексклюзивного блокування (запис).
-   \*\*`LOCK_UN`\*\*для зняття блокування (розділюваного або ексклюзивного).

Також можна додати **`LOCK_NB`** як бітова маска до однієї з вищевказаних операцій, якщо [flock()](function.flock.md) під час спроби блокування не повинен блокуватися.

`wouldBlock`

Будет установлен\*\*`true`\*\*, якщо блокування буде блокуючим (код помилки EWOULDBLOCK).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SplFileObject::flock()\*\*\*\*

```php
<?php
$file = new SplFileObject("/tmp/lock.txt", "w");
if ($file->flock(LOCK_EX)) { // выполняем эксклюзивную блокировку
    $file->ftruncate(0);     // очищаем файл
    $file->fwrite("Что-нибудь пишем сюда\n");
    $file->flock(LOCK_UN);   // снимаем блокировку
} else {
    echo "Не удалось получить блокировку!";
}
?>
```

### Дивіться також

-   [flock()](function.flock.md) \- Портоване консультативне блокування файлів
