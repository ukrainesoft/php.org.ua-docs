- [«EventDnsBase::loadHosts](eventdnsbase.loadhosts.md)
- [EventDnsBase::setOption »](eventdnsbase.setoption.md)

- [PHP Manual](index.md)
- [EventDnsBase](class.eventdnsbase.md)
- Сканує файл у форматі resolv.conf

# EventDnsBase::parseResolvConf

(PECL event \>= 1.2.6-beta)

EventDnsBase::parseResolvConf — Сканує файл у форматі resolv.conf

### Опис

public **EventDnsBase::parseResolvConf**( int `$flags` , string
`$filename` ): bool

Сканує файл у форматі resolv.conf, що зберігається в filename, та зчитує
всі параметри з нього, які перелічені у прапорах.

### Список параметрів

`flags`
Визначає, яка інформація аналізується із файлу `resolv.conf`.
Перегляньте довідкову сторінку `resolv.conf` за форматом цього файлу.

Наступні директиви не аналізуються з файлу:
`sortlist, rotate, no-check-names, inet6, debug`.

Якщо функція виявляє помилку, можливі значення, що повертаються:

- **`1`** = не вдалося відкрити файл
- **`2`** = не вдалося визначити розмір файлу
- **`3`** = файл занадто великий
- **`4`** = недостатньо пам'яті
- **`5`** = коротке читання з файлу
- **`6`** = у файлі немає серверів імен

`filename`
Шлях до `resolv.conf` файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.
