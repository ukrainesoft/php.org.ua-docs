- [«rpmaddtag](function.rpmaddtag.md)
- [rpmdbsearch »](function.rpmdbsearch.md)

- [PHP Manual](index.md)
- [Функції RpmInfo](ref.rpminfo.md)
- Отримує інформацію від встановленого RPM

#rpmdbinfo

(PECL rpminfo => 0.2.0)

rpmdbinfo — Отримує інформацію від встановленого RPM

### Опис

**rpmdbinfo**(string `$nevr`, bool `$full` = **`false`**): array

Отримує інформацію про встановлений пакет із системної бази даних
RPM.

### Список параметрів

`nevr`
Ім'я із зазначенням епохи, версії та випуску.

`full`
Якщо **`true`**, виймаються всі інформаційні заголовки для файлу,
інакше лише мінімальний набір.

### Значення, що повертаються

Масив (array) масивів (array) інформації або NULL у разі
виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **rpmdbinfo()****

` <?phprpmaddtag(RPMTAG_INSTALLTIME);$info = rpmdbinfo("php-pecl-rpminfo");print_r($info);?> `

Результат виконання цього прикладу:

Array
(
[0] => Array
(
[Name] => php-pecl-rpminfo
[Version] => 0.4.2
[Release] => 1.fc31
[Summary] => RPM information
[Installtime] => 1586244687
[Arch] => x86_64
)
)

### Дивіться також

- [rpmaddtag()](function.rpmaddtag.md) - Додає тег, отриманий у
запиті
