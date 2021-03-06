- [«rpmdbsearch](function.rpmdbsearch.md)
- [rpmvercmp »](function.rpmvercmp.md)

- [PHP Manual](index.md)
- [Функції RpmInfo](ref.rpminfo.md)
- Вийняти інформацію з RPM-файлу

# rpminfo

(PECL rpminfo => 0.1.0)

rpminfo — Вийняти інформацію з RPM-файлу

### Опис

**rpminfo**(string `$path`, bool `$full` = **`false`**, string `&$error`
= ?): array

Вийняти інформацію про локальний файл RPM.

### Список параметрів

`path`
Шлях до файлу.

`full`
Якщо **`true`**, то для файлу буде вилучено всі заголовки. Інакше буде
вилучено мінімальний набір.

`error`
Якщо заданий, то нього буде записана інформація про помилку, у разі її
виникнення. Це дозволить уникнути попереджень під час виконання.

### Значення, що повертаються

Масив із даними або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **rpminfo()****

` <?phprpmaddtag(RPMTAG_BUILDTIME);$info = rpminfo("./php-pecl-rpminfo-0.4.2-1.el8.remi.7.4.x86_64.rpm");print_r($info);?> `

Результат виконання цього прикладу:

Array
(
[Name] => php-pecl-rpminfo
[Version] => 0.4.2
[Release] => 1.el8
[Summary] => RPM information
[Buildtime] => 1586244821
[Arch] => x86_64
)

### Дивіться також

- [rpmaddtag()](function.rpmaddtag.md) - Додає тег, отриманий у
запиті
