---
navigation:
  - eio.resources.md: « Типи ресурсів
  - eio.examples.md: Приклади »
  - index.md: PHP Manual
  - book.eio.md: Eio
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Константи пріоритету запиту:

**`EIO_PRI_MIN`**(int)

Мінімальний пріоритет запиту

**`EIO_PRI_DEFAULT`**(int)

Пріоритет за замовчуванням

**`EIO_PRI_MAX`**(int)

Максимальний пріоритет запиту

Аргумент`whence` функції [eio\_seek()](function.eio-seek.md) :

**`EIO_SEEK_SET`**(int)

Смещение`offset`, поставлене в байтах.

**`EIO_SEEK_CUR`**(int)

Смещение`offset`, заданий у байтах від поточного значення.

**`EIO_SEEK_END`**(int)

Смещение`offset`, заданий у байтах від розміру файлу.

Прапори, що використовуються в [eio\_readdir()](function.eio-readdir.md) :

**`EIO_READDIR_DENTS`**(int)

Флаг[eio\_readdir()](function.eio-readdir.md). Якщо вказано, аргумент для виконання callback-функції стає масивом із такими ключами: `'names'` - масив імен директорії `'dents'`\- массив массивов вида`struct eio_dirent`, кожен з яких має ключі: `'name'` - Ім'я директорії; `'type'`\- одна из констант*EIO\_DT\_\** `'inode'` - Номер inode, якщо він доступний, інакше значення не вказується;

**`EIO_READDIR_DIRS_FIRST`**(int)

Коли прапор вказано, імена будуть повернуті у порядку, у якому будуть повернуті першими директорії оптимальному порядку.

**`EIO_READDIR_STAT_ORDER`**(int)

Коли прапор вказано, імена будуть повернуті у порядку, залежно від `stat` кожного із них. Якщо планується виконати [stat()](function.stat.md) для всіх файлів у директорії, такий порядок буде, швидше за все, найшвидшим.

**`EIO_READDIR_FOUND_UNKNOWN`**(int)

**`EIO_DT_UNKNOWN`**(int)

Невідомий тип вузла (дуже поширене). Далі потрібен виклик [stat()](function.stat.md)

**`EIO_DT_FIFO`**(int)

Тип FIFO вузла

**`EIO_DT_CHR`**(int)

Тип вузла

**`EIO_DT_MPC`**(int)

Тип вузла мультиплексний символьний пристрій (v7+coherent)

**`EIO_DT_DIR`**(int)

Тип вузла директорія

**`EIO_DT_NAM`**(int)

Тип вузла - спеціальний іменований файл Xenix (Xenix special named file)

**`EIO_DT_BLK`**(int)

Тип вузла

**`EIO_DT_MPB`**(int)

Тип вузла мультиплексний блоковий пристрій (Multiplexed block device) (v7+coherent)

**`EIO_DT_REG`**(int)

Тип вузла

**`EIO_DT_NWK`**(int)

**`EIO_DT_CMP`**(int)

Тип вузла HP-UX network special

**`EIO_DT_LNK`**(int)

Тип вузла посилання

**`EIO_DT_SOCK`**(int)

Тип вузла сокет

**`EIO_DT_DOOR`**(int)

Тип вузла Solaris door

**`EIO_DT_WHT`**(int)

Тип вузла

**`EIO_DT_MAX`**(int)

Найбільше значення типу вузла

Режими доступу для [eio\_open()](function.eio-open.md)аргумент`flags` :

**`EIO_O_RDONLY`**(int)

**`EIO_O_WRONLY`**(int)

**`EIO_O_RDWR`**(int)

**`EIO_O_NONBLOCK`**(int)

**`EIO_O_APPEND`**(int)

**`EIO_O_CREAT`**(int)

**`EIO_O_TRUNC`**(int)

**`EIO_O_EXCL`**(int)

**`EIO_O_FSYNC`**(int)

Флаги аргумента`mode` функції [eio\_open()](function.eio-open.md) :

**`EIO_S_IRUSR`**(int)

**`EIO_S_IWUSR`**(int)

**`EIO_S_IXUSR`**(int)

**`EIO_S_IRGRP`**(int)

**`EIO_S_IWGRP`**(int)

**`EIO_S_IXGRP`**(int)

**`EIO_S_IROTH`**(int)

**`EIO_S_IWOTH`**(int)

**`EIO_S_IXOTH`**(int)

**`EIO_S_IFREG`**(int)

**`EIO_S_IFCHR`**(int)

**`EIO_S_IFBLK`**(int)

**`EIO_S_IFIFO`**(int)

**`EIO_S_IFSOCK`**(int)

Флаги функции[eio\_sync\_file\_range()](function.eio-sync-file-range.md) :

**`EIO_SYNC_FILE_RANGE_WAIT_BEFORE`**(int)

**`EIO_SYNC_FILE_RANGE_WRITE`**(int)

**`EIO_SYNC_FILE_RANGE_WAIT_AFTER`**(int)

Флаги функции[eio\_fallocate()](function.eio-fallocate.md) :

**`EIO_FALLOC_FL_KEEP_SIZE`**(int)

> **Зауваження** :
> 
> Константи *EIO\_S\_I\** мають те саме значення, що їхні колеги \*S\_I\*\*в POSIX.

> **Зауваження** :
> 
> *EIO\_SYNC\_FILE\_\** мають те саме значення, що їхні колеги *SYNC\_FILE\_\*\**

> **Зауваження** :
> 
> *EIO\_O\_\** мають те саме значення, що їхні колеги \*O\_\*\*в POSIX.
