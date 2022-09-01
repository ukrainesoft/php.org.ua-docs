---
navigation:
  - eventdnsbase.loadhosts.md: '« EventDnsBase::loadHosts'
  - eventdnsbase.setoption.md: 'EventDnsBase::setOption »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::parseResolvConf'
---
# EventDnsBase::parseResolvConf

(PECL event >= 1.2.6-beta)

EventDnsBase::parseResolvConf — Сканує файл у форматі resolv.conf

### Опис

```methodsynopsis
public
   EventDnsBase::parseResolvConf(
    int
     $flags
   , 
    string
     $filename
   ): bool
```

Сканує файл у форматі resolv.conf, що зберігається в filename, і зчитує всі параметри з нього, які перелічені у прапорах.

### Список параметрів

`flags`

Визначає, яка інформація аналізується із файлу `resolv.conf`. Дивіться довідкову сторінку `resolv.conf` формат цього файлу.

Наступні директиви не аналізуються з файлу: `sortlist, rotate, no-check-names, inet6, debug`

Якщо функція виявляє помилку, можливі значення, що повертаються:

-   **`1`** = Не вдалося відкрити файл
-   **`2`** = не вдалося визначити розмір файлу
-   **`3`** = файл занадто великий
-   **`4`** = недостатньо пам'яті
-   **`5`** = коротке читання з файлу
-   **`6`** = у файлі немає серверів імен

`filename`

Шлях до `resolv.conf` файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
