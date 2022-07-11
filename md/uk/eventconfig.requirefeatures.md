- [«EventConfig::\_\_construct](eventconfig.construct.md)
- [EventConfig::setFlags »](eventconfig.setflags.md)

- [PHP Manual](index.md)
- [EventConfig](class.eventconfig.md)
- Ввести необхідні додатком властивості методу події

# EventConfig::requireFeatures

(PECL event \>= 1.2.6-beta)

EventConfig::requireFeatures — Ввести потрібні додатком властивості
методу події

### Опис

public **EventConfig::requireFeatures**( int `$feature` ): bool

Вводить необхідну програмою функціональність методу події

### Список параметрів

`feature`
Бітова маска потрібних властивостей. Дивіться [константи `EventConfig::FEATURE_*`](class.eventconfig.md#eventconfig.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventConfig::requireFeatures()****

` <?php$cfg = new EventConfig();// Створюємо event_base, пов'язаний з конфігом $cfg$base = neu EventBase($cfg);// Запрошуємо Fs {    echo "Властивість FDS запрошено
";   $base = new EventBase($cfg);    ($base->getFeatures() & EventConfig::FEATURE_FDS)         and print("FDS и
");}?> `

Результатом виконання цього прикладу буде щось подібне:

Властивість FDS запитана
FDS – довільні типи дескрипторів файлів, а не тільки сокети

### Дивіться також

- [EventBase::getFeatures()](eventbase.getfeatures.md) - Повертає
бітову маску підтримуваних функцій
