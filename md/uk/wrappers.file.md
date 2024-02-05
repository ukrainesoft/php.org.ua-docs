---
navigation:
  - wrappers.md: « Підтримувані протоколи та обгортки
  - wrappers.http.md: 'http:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'file://'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# file://

file:// — Доступ до локальної файлової системи

### Опис

*Файлова система* - це стандартна обгортка для PHP, що представляє файлову систему на локальному комп'ютері. Коли заданий відносний шлях (шлях, який не починається із символів "/", "\\", "\\\\" або з літери жорсткого диска в Windows), він буде застосований до поточної робочої директорії. У більшості випадків це директорія, в якій знаходиться сценарій, якщо вона не була змінена. При використанні CLI SAPI директорією за замовчуванням буде та, з якої викликано виконання сценарію .

У деяких функціях, таких як [fopen()](function.fopen.md) і [file\_get\_contents()](function.file-get-contents.md), пошук файлу може додатково проводитися в `include_path`

### Використання

-   /path/to/file.ext
-   relative/path/to/file.ext
-   fileInCwd.ext
-   C:/path/to/winfile.ext
-   C:\\path\\to\\winfile.ext
-   \\\\smbserver\\share\\path\\to\\winfile.ext
-   file:///path/to/file.ext

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.md#ini.allow-url-fopen) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Так |
| Одночасне читання та запис | Так |
| Поддержка[stat()](function.stat.md) | Так |
| Поддержка[unlink()](function.unlink.md) | Так |
| Поддержка[rename()](function.rename.md) | Так |
| Поддержка[mkdir()](function.mkdir.md) | Так |
| Поддержка[rmdir()](function.rmdir.md) | Так |
