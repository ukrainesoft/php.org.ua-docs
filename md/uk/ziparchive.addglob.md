---
navigation:
  - ziparchive.addfromstring.md: '« ZipArchive::addFromString'
  - ziparchive.addpattern.md: 'ZipArchive::addPattern »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::addGlob'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::addGlob

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL zip >= 1.9.0)

ZipArchive::addGlob — Додати файли з директорії відповідно до шаблону

### Опис

```methodsynopsis
public ZipArchive::addGlob(string $pattern, int $flags = 0, array $options = []): array|false
```

Додати файли з директорії відповідно до шаблону `pattern`

> **Зауваження**: Для максимальної переносимості, рекомендується завжди використовувати прямі сліші ( ) як роздільник директорій в іменах файлів.

### Список параметрів

`pattern`

Шаблон функции[glob()](function.glob.md), за яким вибиратимуться файли.

`flags`

Бітова маска прапорів `glob()`

`options`

Асоціативний масив опцій. Доступні значення:

-   `"add_path"`
    
    Префікс, який додаватиметься на початок локального шляху в архіві. Накладається після застосування операцій, заданих у`"remove_path"`или`"remove_all_path"`
    
-   `"remove_path"`
    
    Префікс, який буде видалено з дороги перед додаванням до архіву.
    
-   `"remove_all_path"`
    
    Встановіть як\*\*`true`\*\*для використання лише імені файлів та складання їх у корінь архіву.
    
-   `"flags"`
    
    Бітова маска, що складається з **`ZipArchive::FL_OVERWRITE`** **`ZipArchive::FL_ENC_GUESS`** **`ZipArchive::FL_ENC_UTF_8`** **`ZipArchive::FL_ENC_CP437`** \*\*`ZipArchive::FL_OPEN_FILE_NOW`\*\*Поведение констант описано на странице[ZIP-константи](zip.constants.md)
    
-   `"comp_method"`
    
    Метод сжатия, одна из констант\*\*`ZipArchive::CM_*`\*\*, дивіться сторінку[константи ZIP](zip.constants.md)
    
-   `"comp_flags"`
    
    Рівень стиску.
    
-   `"enc_method"`
    
    Метод шифрования, одна из констант\*\*`ZipArchive::EM_*`\*\*, дивіться сторінку[константи ZIP](zip.constants.md)
    
-   `"enc_password"`
    
    Пароль для шифрування.
    

### Значення, що повертаються

Масив (array) доданих файлів у разі успішного виконання або **`false`** у разі виникнення помилки Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 / 1.18.0 | Добавлен параметр`"flags"`в`options` |
| 8.0.0 / 1.18.1 | Додані параметри `"comp_method"` `"comp_flags"` `"enc_method"`и`"enc_password"`в`options` |
| 8.3.0 / 1.22.1 | Добавлена константа\*\*`ZipArchive::FL_OPEN_FILE_NOW`\*\* |

### Приклади

**Приклад #1 Приклад використання** ZipArchive::addGlob()\*\*\*\*

Додати до архіву всі текстові файли та файли скриптів PHP з поточної директорії

```php
<?php
$zip = new ZipArchive();
$ret = $zip->open('application.zip', ZipArchive::CREATE | ZipArchive::OVERWRITE);
if ($ret !== TRUE) {
    printf('Ошибка с кодом %d', $ret);
} else {
    $options = array('add_path' => 'sources/', 'remove_all_path' => TRUE);
    $zip->addGlob('*.{php,txt}', GLOB_BRACE, $options);
    $zip->close();
}
?>
```

### Дивіться також

-   [ZipArchive::addFile()](ziparchive.addfile.md) \- Додає до ZIP-архіву файл по зазначеному шляху
-   [ZipArchive::addPattern()](ziparchive.addpattern.md) \- Додати файли з директорії відповідно до шаблону регулярного вираження PCRE
