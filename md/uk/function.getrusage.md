---
navigation:
  - function.getopt.md: « getopt
  - function.ini-alter.md: ini\_alter »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: getrusage
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# getrusage

(PHP 4, PHP 5, PHP 7, PHP 8)

getrusage — Отримує інформацію про використання поточного ресурсу

### Опис

```methodsynopsis
getrusage(int $mode = 0): array|false
```

Це інтерфейс до **getrusage(2)**. Функція отримує дані, що повертаються із системного виклику.

### Список параметрів

`mode`

Якщо аргумент `mode` дорівнює 1, getrusage буде викликана з **`RUSAGE_CHILDREN`**

### Значення, що повертаються

Повертає асоціативний масив, що містить дані, повернені із системного виклику. Імена елементів відповідають документованим іменам полів. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.0.0 | Додано підтримку цієї функції у Windows. |

### Приклади

**Пример #1 Пример использования**getrusage()\*\*\*\*

```php
<?php
$dat = getrusage();
echo $dat["ru_oublock"];       // количество операций вывода блока
echo $dat["ru_inblock"];       // количество операций приёма блока
echo $dat["ru_msgsnd"];        // количество отправленных сообщений IPC
echo $dat["ru_msgrcv"];        // количество принятых сообщений IPC
echo $dat["ru_maxrss"];        // наибольший размер установленной резидентной памяти
echo $dat["ru_ixrss"];         // суммарное значение размера разделяемой памяти
echo $dat["ru_idrss"];         // суммарное значение размера неразделяемых данных
echo $dat["ru_minflt"];        // количество исправленных страниц (лёгкая ошибка страницы)
echo $dat["ru_majflt"];        // количество ошибочных страниц (тяжёлая ошибка страницы)
echo $dat["ru_nsignals"];      // количество полученных сигналов
echo $dat["ru_nvcsw"];         // количество согласованных переключений контекста
echo $dat["ru_nivcsw"];        // количество несогласованных переключений контекста
echo $dat["ru_nswap"];         // количество свопов
echo $dat["ru_utime.tv_usec"]; // время на задачи пользователя (user time) (микросекунды)
echo $dat["ru_utime.tv_sec"];  // время на задачи пользователя (user time) (секунды)
echo $dat["ru_stime.tv_usec"]; // время на системные задачи (system time) (микросекунды)
echo $dat["ru_stime.tv_sec"];  // время на системные задачи (system time) (секунды)
?>
```

### Примітки

> **Зауваження** :
> 
> В Windows**getrusage()** повертає лише таке:
> 
> -   `"ru_stime.tv_sec"`
> -   `"ru_stime.tv_usec"`
> -   `"ru_utime.tv_sec"`
> -   `"ru_utime.tv_usec"`
> -   `"ru_majflt"`(тільки якщо`mode` **`RUSAGE_SELF`**) .
> -   `"ru_maxrss"`(тільки якщо`mode` **`RUSAGE_SELF`**) .
> 
> Якщо **getrusage()** викликана з `mode` рівним **`RUSAGE_CHILDREN`**), то буде збиратися інформація щодо використання ресурсів потоками (що означає, що всередині функція буде викликатися з **`RUSAGE_THREAD`**

> **Зауваження** :
> 
> У BeOS 2000, повертається лише таке:
> 
> -   `"ru_stime.tv_sec"`
> -   `"ru_stime.tv_usec"`
> -   `"ru_utime.tv_sec"`
> -   `"ru_utime.tv_usec"`

### Дивіться також

-   Сторінка системної документації**getrusage(2)**
