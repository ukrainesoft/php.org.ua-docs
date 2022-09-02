---
navigation:
  - streamwrapper.dir-readdir.md: '« streamWrapper::dirreaddir'
  - streamwrapper.mkdir.md: 'streamWrapper::mkdir »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::dirrewinddir'
---
# streamWrapper::dirrewinddir

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::dirrewinddir - Дескриптор директорії переміщення на її початок

### Опис

```methodsynopsis
public streamWrapper::dir_rewinddir(): bool
```

Цей метод викликається у процесі виконання [rewinddir()](function.rewinddir.md)

Повинен скидати поточний висновок, що генерується методом [streamWrapper::dirreaddir()](streamwrapper.dir-readdir.md). Тобто. при наступному виклику метод [streamWrapper::dirreaddir()](streamwrapper.dir-readdir.md) повинен повертати перший запис у директорії, визначеній методом [streamWrapper::diropendir()](streamwrapper.dir-opendir.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [rewinddir()](function.rewinddir.md) - Скинути дескриптор каталогу
-   [streamWrapper::dirreaddir()](streamwrapper.dir-readdir.md) - Читання запису з дескриптора директорії
