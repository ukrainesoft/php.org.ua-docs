---
navigation:
  - function.dio-seek.md: « dio\_seek
  - function.dio-tcsetattr.md: dio\_tcsetattr »
  - index.md: PHP Manual
  - ref.dio.md: Функції прямого введення/виводу
title: dio\_stat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dio\_stat

(PHP 4 >= 4.2.0, PHP 5 < 5.1.0)

dio\_stat — Отримати інформацію про файловий дескриптор

### Опис

```methodsynopsis
dio_stat(resource $fd): array
```

**dio\_stat()** повертає інформацію про заданий дескриптор.

### Список параметрів

`fd`

Файловий дескриптор, отриманий з [dio\_open()](function.dio-open.md)

### Значення, що повертаються

Повертає асоціативний масив із такими ключами:

-   "device" - пристрій
    
-   "inode" - inode
    
-   "mode" - права доступу
    
-   "nlink" - кількість жорстких посилань
    
-   "uid" - ідентифікатор користувача
    
-   "Gid" - ідентифікатор групи
    
-   "device\_type" - тип пристрою (якщо воно inode)
    
-   "size" - розмір у байтах
    
-   "blocksize" - розмір блоку
    
-   "blocks" - кількість виділених блоків
    
-   "atime" - час останнього доступу
    
-   "mtime" - час останньої модифікації
    
-   "ctime" - час останньої зміни
    

В случае возникновения ошибки**dio\_stat()** поверне **`null`**
