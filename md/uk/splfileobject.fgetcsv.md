Отримати рядок із файлу та його розбір як поля CSV

-   [« SplFileObject::fgetc](splfileobject.fgetc.html)
    
-   [SplFileObject::fgets »](splfileobject.fgets.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Отримати рядок із файлу та його розбір як поля CSV
    

# SplFileObject::fgetcsv

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fgetcsv — Отримати рядок із файлу та його розбір як поля CSV

### Опис

```methodsynopsis
public SplFileObject::fgetcsv(string $separator = ",", string $enclosure = "\"", string $escape = "\\"): array|false
```

Отримує рядок із файлу та розбирає його відповідно до формату CSV. Результати аналізу повертає у вигляді масиву.

> **Зауваження**
> 
> Ця функція враховує налаштування локалі. Наприклад, якщо `LC_CTYPE` встановлена ​​в `en_US.UTF-8`, то файли в однобайтовому кодуванні будуть неправильно прочитані цією функцією.

### Список параметрів

`separator`

Розділювач полів (тільки один однобайтовий символ). За замовчуванням це кома або символ, заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.html)

`enclosure`

Символ обмежувача поля (лише один однобайтовий символ). За замовчуванням це подвійна лапка або символ, заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.html). Порожня стрічка (`""`) відключає пропрієтарний механізм екранування.

> **Зауваження**: Зазвичай символ `enclosure` екранується всередині поля шляхом його подвоювання; однак, символ `escape` як альтернатива. Тому значення за промовчанням цих параметрів `""` і `\"` мають однакове значення. Крім дозволу екранувати символ `enclosure` символ `escape` немає особливого сенсу; він навіть не призначений для самого екранування.

`escape`

Екрануючий символ (не більше одного однобайтового символу). За замовчуванням це зворотний сліш (`\`) або символ, який був заданий методом [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.html)

### Значення, що повертаються

Повертає масив містить дані прочитаного рядка або **`false`** у разі помилки.

> **Зауваження**
> 
> Порожній рядок CSV-файлу повертатиметься у вигляді масиву, що містить єдиний елемент **`null`**, якщо не використовується **`SplFileObject::SKIP_EMPTY | SplFileObject::DROP_NEW_LINE`**, і в цьому випадку порожні рядки пропускаються.

### список змін

| Версия | Описание                                                                                                 |
|--------|----------------------------------------------------------------------------------------------------------|
|        | Тепер параметр `escape` може приймати порожній рядок для вимкнення пропрієтарного механізму екранування. |

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fgetcsv()****

```php
<?php
$file = new SplFileObject("data.csv");
while (!$file->eof()) {
    var_dump($file->fgetcsv());
}
?>
```

**Приклад #2 Приклад використання **`SplFileObject::READ_CSV`****

```php
<?php
$file = new SplFileObject("animals.csv");
$file->setFlags(SplFileObject::READ_CSV);
foreach ($file as $row) {
    list($animal, $class, $legs) = $row;
    printf("A %s is a %s with %d legs\n", $animal, $class, $legs);
}
?>
```

Contents of animals.csv

crocodile,reptile,4 dolphin,mammal,0 duck,bird,2 koala,mammal,4 salmon,fish,0

Результатом виконання цього прикладу буде щось подібне:

```
A crocodile is a reptile with 4 legs
A dolphin is a mammal with 0 legs
A duck is a bird with 2 legs
A koala is a mammal with 4 legs
A salmon is a fish with 0 legs
```

### Дивіться також

-   [SplFileObject::setCsvControl()](splfileobject.setcsvcontrol.html) - Встановлює символи роздільника, обгортання та екранування для CSV
-   [SplFileObject::setFlags()](splfileobject.setflags.html) - Встановлює прапори для SplFileObject
-   [SplFileObject::READ\_CSV](class.splfileobject.html#splfileobject.constants.read-csv)
-   [SplFileObject::current()](splfileobject.current.html) - Отримати поточний рядок файлу