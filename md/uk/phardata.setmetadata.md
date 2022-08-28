Встановити метадані phar-архіву

-   [« PharData::setDefaultStub](phardata.setdefaultstub.html)
    
-   [PharData::setSignatureAlgorithm »](phardata.setsignaturealgorithm.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Встановити метадані phar-архіву
    

# PharData::setMetadata

(No version information available, might only be in Git)

PharData::setMetadata — Встановити метадані phar-архіву

### Опис

```methodsynopsis
public PharData::setMetadata(mixed $metadata): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Функція [Phar::setMetadata()](phar.setmetadata.html) використовується для збереження даних, що характеризують phar-архів загалом . [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.html) використовується для встановлення метаданих для файлу. Якщо метаданих буде багато, це може знизити швидкість завантаження phar-архіву.

Метадані можна використовувати, наприклад, для вказівки, який файл повинен виконуватися під час завантаження, або для вказівки розташування маніфесту, типу package.xml для модуля [» PEAR](https://pear.php.net/). Загалом будь-які корисні в контексті phar-архіву дані.

### Список параметрів

`metadata`

Будь-яка змінна PHP, що містить необхідну інформацію

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання [Phar::setMetadata()](phar.setmetadata.html)**

```php
<?php
// удаляем, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "hello"';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Не удалось создать и/или изменить phar:', $e;
}
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["bootstrap"]=>
  string(8) "file.php"
}
```

### Дивіться також

-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву
-   [Phar::delMetadata()](phar.delmetadata.html) - Видалити глобальні метадані в архіві phar
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані