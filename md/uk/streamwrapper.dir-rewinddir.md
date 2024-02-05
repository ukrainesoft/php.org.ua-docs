---
navigation:
  - streamwrapper.dir-readdir.md: '« streamWrapper::dir\_readdir'
  - streamwrapper.mkdir.md: 'streamWrapper::mkdir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::dir\_rewinddir'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::dir\_rewinddir

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dir\_rewinddir - Дескриптор директорії переміщення на її початок

### Опис

```methodsynopsis
public streamWrapper::dir_rewinddir(): bool
```

Цей метод викликається у процесі виконання [rewinddir()](function.rewinddir.md)

Повинен скидати поточний висновок, що генерується методом [streamWrapper::dir\_readdir()](streamwrapper.dir-readdir.md). Тобто. при наступному виклику метод [streamWrapper::dir\_readdir()](streamwrapper.dir-readdir.md) повинен повертати перший запис у директорії, визначеній методом [streamWrapper::dir\_opendir()](streamwrapper.dir-opendir.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [rewinddir()](function.rewinddir.md) \- Скинути дескриптор каталогу
-   [streamWrapper::dir\_readdir()](streamwrapper.dir-readdir.md) \- Читання запису з дескриптора директорії
