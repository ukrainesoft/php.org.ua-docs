---
navigation:
  - splfileobject.fgetc.md: '« SplFileObject::fgetc'
  - splfileobject.fgets.md: 'SplFileObject::fgets »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fgetcsv'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fgetcsv

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fgetcsv — Отримати рядок із файлу та його розбір як поля CSV

### Опис

```methodsynopsis
public SplFileObject::fgetcsv(string $separator = ",", string $enclosure = "\"", string $escape = "\\"): array|false
```

Отримує рядок із файлу та розбирає його відповідно до формату CSV. Результати аналізу повертає у вигляді масиву.

> **Зауваження** :
> 
> Ця функція враховує налаштування локалі. Наприклад, якщо `LC_CTYPE`установлена в`en_US.UTF-8`, то файли в однобайтовому кодуванні будуть неправильно прочитані цією функцією.

### Список параметрів

`separator`

Розділювач полів (тільки один однобайтовий символ). За замовчуванням це кома або символ, заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md)

`enclosure`

Символ обмежувача поля (лише один однобайтовий символ). За замовчуванням це подвійна лапка або символ, заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md). Порожня стрічка (`""`) відключає пропрієтарний механізм екранування.

> **Зауваження**: Зазвичай символ `enclosure` екранується всередині поля шляхом його подвоювання; однак, символ `escape` як альтернатива. Тому значення за промовчанням цих параметрів `""`и`\"` мають однакове значення. Крім дозволу екранувати символ `enclosure`символ`escape` немає особливого сенсу; він навіть не призначений для самого екранування.

`escape`

Екрануючий символ (не більше одного однобайтового символу). За замовчуванням це зворотний сліш (`\`) або символ, який був заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md)

### Значення, що повертаються

Повертає масив містить дані прочитаного рядка або \*\*`false`\*\*в случае ошибки.

> **Зауваження** :
> 
> Порожній рядок CSV-файлу повертатиметься у вигляді масиву, що містить єдиний елемент **`null`**, якщо не використовується **`SplFileObject::SKIP_EMPTY | SplFileObject::DROP_NEW_LINE`**, і в цьому випадку порожні рядки пропускаються.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Тепер параметр `escape` може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |

### Приклади

**Пример #1 Пример использования**SplFileObject::fgetcsv()\*\*\*\*

```php
<?php
$file = new SplFileObject("data.csv");
while (!$file->eof()) {
    var_dump($file->fgetcsv());
}
?>
```

**Пример #2 Пример использования**`SplFileObject::READ_CSV`\*\*\*\*

```php
<?php
$file = new SplFileObject("animals.csv");
$file->setFlags(SplFileObject::READ_CSV);
foreach ($file as $row) {
    list($animal, $class, $legs) = $row;
    printf("A %s is a %s with %d legs\n", $animal, $class, $legs);
}
?>
```

Contents of animals.csv

crocodile,reptile,4 dolphin,mammal,0 duck,bird,2 koala,mammal,4 salmon,fish,0

Висновок наведеного прикладу буде схожим на:

```
A crocodile is a reptile with 4 legs
A dolphin is a mammal with 0 legs
A duck is a bird with 2 legs
A koala is a mammal with 4 legs
A salmon is a fish with 0 legs
```

### Дивіться також

-   [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.md) \- Встановлює символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::setFlags()](splfileobject.setflags.md) \- Встановлює прапори для SplFileObject
-   [SplFileObject::READ\_CSV](class.splfileobject.md#splfileobject.constants.read-csv)
-   [SplFileObject::current()](splfileobject.current.md) \- Отримати поточний рядок файлу
