Встановлює параметри конфігурації libmagic

-   [« finfo\_open](function.finfo-open.html)
    
-   [mime\_content\_type »](function.mime-content-type.html)
    
-   [PHP Manual](index.html)
    
-   [Функции модуля Fileinfo](ref.fileinfo.html)
    
-   Встановлює параметри конфігурації libmagic
    

# finfosetflags

# finfo::setflags

(PHP >= 5.3.0, PHP 7, PHP 8, PECL fileinfo >= 0.1.0)

finfosetflags -- finfo::setflags — Встановлює параметри конфігурації libmagic

### Опис

Процедурний стиль

```methodsynopsis
finfo_set_flags(finfo $finfo, int $flags): bool
```

Об'єктно-орієнтований стиль

```methodsynopsis
public finfo::set_flags(int $flags): bool
```

Функція встановлює різні параметри FileInfo. Опції також можуть бути встановлені безпосередньо в [finfo\_open()](function.finfo-open.html) або інших функцій Fileinfo.

### Список параметрів

`finfo`

Екземпляр [finfo](class.finfo.html), що повертається функцією [finfo\_open()](function.finfo-open.html)

`flags`

Одна або кілька об'єднаних через бінарне АБО [констант Fileinfo](fileinfo.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `finfo` тепер чекає екземпляр [finfo](class.finfo.html); раніше очікувався ресурс ([resource](language.types.resource.html) |