---
navigation:
  - filesystem.resources.md: « Типи ресурсів
  - ref.filesystem.md: Функції файлової системи »
  - index.md: PHP Manual
  - book.filesystem.md: Файлова система
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SEEK_SET`**(int)

**`SEEK_CUR`**(int)

**`SEEK_END`**(int)

**`LOCK_SH`**(int)

**`LOCK_EX`**(int)

**`LOCK_UN`**(int)

**`LOCK_NB`**(int)

**`GLOB_BRACE`**(int)

**`GLOB_ONLYDIR`**(int)

**`GLOB_MARK`**(int)

**`GLOB_NOSORT`**(int)

**`GLOB_NOCHECK`**(int)

**`GLOB_NOESCAPE`**(int)

**`GLOB_AVAILABLE_FLAGS`**(int)

**`PATHINFO_DIRNAME`**(int)

**`PATHINFO_BASENAME`**(int)

**`PATHINFO_EXTENSION`**(int)

**`PATHINFO_FILENAME`**(int)

**`FILE_USE_INCLUDE_PATH`**(int)

Шукає `filename`в[include\_path](ini.core.md#ini.include-path)

**`FILE_NO_DEFAULT_CONTEXT`**(int)

**`FILE_APPEND`**(int)

Додає дані до наявного файлу.

**`FILE_IGNORE_NEW_LINES`**(int)

Вирізають кінці рядків (EOL).

**`FILE_SKIP_EMPTY_LINES`**(int)

Пропускаються порожні рядки.

**`FILE_BINARY`**(int)

Бінарний режим.

> **Зауваження** :
> 
> Ця константа ні на що не впливає і доступна тільки для подальшої сумісності (`forward compatibility`

**`FILE_TEXT`**(int)

Текстовий режим.

> **Зауваження** :
> 
> Ця константа ні на що не впливає і доступна тільки для подальшої сумісності (`forward compatibility`

**`INI_SCANNER_NORMAL`**(int)

Звичайний режим сканування INI.

**`INI_SCANNER_RAW`**(int)

Режим необробленого сканування INI.

**`INI_SCANNER_TYPED`**(int)

Типовий режим сканування INI.

**`FNM_NOESCAPE`**(int)

Вимикає екранування зворотних слішів.

**`FNM_PATHNAME`**(int)

Сліші у рядках збігаються тільки зі слішами у вказаному шаблоні.

**`FNM_PERIOD`**(int)

Ведуча точка в рядку повинна точно збігатися з точкою у вказаному шаблоні.

**`FNM_CASEFOLD`**(int)

Збіг без урахування регістру. Частина розширення GNU.
