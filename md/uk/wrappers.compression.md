---
navigation:
  - wrappers.php.md: '« php://'
  - wrappers.data.md: 'data:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'zlib://'
---
# zlib://

# bzip2://

# zip://

zlib:// -- bzip2:// -- zip:// -- Стислі потоки

### Опис

compress.zlib:// та compress.bzip2://

zlib: працює як [gzopen()](function.gzopen.md) крім того, що цей потік може використовуватися функцією [fread()](function.fread.md) та іншими функціями, що працюють із файловою системою. Застаріла через неоднозначність за наявності файлів, що містять ':'; використовуйте замість compress.zlib://.

compress.zlib:// та compress.bzip2:// еквіваленти [gzopen()](function.gzopen.md) і [bzopen()](function.bzopen.md) відповідно і працюють навіть у системах, що не підтримують fopencookie.

[Модуль ZIP](book.zip.md) додає обгортку zip:. Починаючи з PHP 7.2.0 та libzip 1.2.0+, було додано підтримку паролів для зашифрованих архівів, дозволяючи надавати паролі, використовуючи контексти потоків. Паролі можуть бути встановлені за допомогою контекстної опції `'password'`

### Використання

-   compress.zlib://file.gz
-   compress.bzip2://file.bz2
-   zip://archive.zip#dir/file.txt

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Читання | Так |
| Запис | Так (крім `zip://` |
| Додавання | Так (крім `zip://` |
| Одночасне читання та запис | Ні |
| Підтримка [stat()](function.stat.md) | Ні, використовуйте стандартну обгортку `file://` для отримання інформації щодо стислих файлів. |
| Підтримка [unlink()](function.unlink.md) | Ні, використовуйте стандартну обгортку `file://` видалення стислих файлів. |
| Підтримка [rename()](function.rename.md) | Ні |
| Підтримка [mkdir()](function.mkdir.md) | Ні |
| Підтримка [rmdir()](function.rmdir.md) | Ні |
