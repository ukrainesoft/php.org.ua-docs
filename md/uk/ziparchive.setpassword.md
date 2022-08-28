Встановлення пароля для активного архіву

-   [« ZipArchive::setMtimeName](ziparchive.setmtimename.html)
    
-   [ZipArchive::statIndex »](ziparchive.statindex.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Встановлення пароля для активного архіву
    

# ZipArchive::setPassword

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL zip >= 1.12.4)

ZipArchive::setPassword — Встановлення пароля для активного архіву

### Опис

```methodsynopsis
public ZipArchive::setPassword(string $password): bool
```

Вказує пароль для активного архіву.

### Список параметрів

`password`

Пароль для архіву.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Примітки

> **Зауваження**
> 
> Починаючи з PHP 7.2.0 і libzip 1.2.0, пароль використовується для розпакування архіву, а також як пароль за замовчуванням для [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.html) і [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.html). Раніше ця функція встановлювала пароль лише для розпакування. Вона не перетворювала не захищений паролем [ZipArchive](class.ziparchive.html) у захищений [ZipArchive](class.ziparchive.html)

### Дивіться також

-   [ZipArchive::setEncryptionIndex()](ziparchive.setencryptionindex.html) - Встановити метод шифрування запису за його індексом
-   [ZipArchive::setEncryptionName()](ziparchive.setencryptionname.html) - Встановити метод шифрування запису на його ім'я