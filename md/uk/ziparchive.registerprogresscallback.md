Реєструє callback-функцію для надання оновлень під час закриття архіву

-   [« ZipArchive::registerCancelCallback](ziparchive.registercancelcallback.html)
    
-   [ZipArchive::renameIndex »](ziparchive.renameindex.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Реєструє callback-функцію для надання оновлень під час закриття архіву
    

# ZipArchive::registerProgressCallback

(PHP >= 8.0.0, PECL zip >= 1.17.0)

ZipArchive::registerProgressCallback — Реєструє callback-функцію для надання оновлень під час закриття архіву

### Опис

```methodsynopsis
public ZipArchive::registerProgressCallback(float $rate, callable $callback): bool
```

Реєструє `callback`функцію надання оновлень при закритті архіву.

### Список параметрів

`rate`

Зміна між кожним викликом callback-функції (від 0,0 до 1,0).

`callback`

Функція отримуватиме поточний стан (`state`) у вигляді числа з плаваючою точкою (float) (від 0,0 до 1,0).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

У цьому прикладі створюється ZIP-архів php.zip та відображається прогресія.

**Приклад #1 Архівація файлу**

```php
$zip = new ZipArchive();
if ($zip->open('php.zip', ZipArchive::CREATE | ZipArchive::OVERWRITE)) {
    $zip->addFile(PHP_BINARY, 'php');
    $zip->registerProgressCallback(0.05, function ($r) {
        printf("%d%%\n", $r * 100);
    });
    $zip->close();
}
```

### Примітки

> **Зауваження**
> 
> Функція доступна, якщо PHP скомпільовано з libzip ≥ 1.6.0.

### Дивіться також

-   [ZipArchive::registerCancelCallback()](ziparchive.registercancelcallback.html) - Реєструє callback-функцію для дозволу скасування під час закриття архіву