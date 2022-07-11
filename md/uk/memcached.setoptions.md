- [« Memcached::setOption](memcached.setoption.md)
- [Memcached::setSaslAuthData »](memcached.setsaslauthdata.md)

- [PHP Manual](index.md)
- [Memcached](class.memcached.md)
- Встановлює кілька Memcached параметрів

# Memcached::setOptions

(PECL memcached \>= 2.0.0)

Memcached::setOptions — Встановлює кілька параметрів Memcached

### Опис

public **Memcached::setOptions**(array `$options`): bool

**Memcached::setOptions()** аналогічний методу
[Memcached::setOption()](memcached.setoption.md), але приймає масив
параметрів.

### Список параметрів

`options`
Асоціативний масив з параметрами, де як ключ виступає
назва параметра, а як значення- нове значення даного
параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлює декілька Memcached параметрів**

` <?php$m = new Memcached();var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);$m->setOptions(array(Memcached::OPT_HASH ) HASH_MURMUR, Memcached::OPT_PREFIX_KEY => "widgets"));var_dump($m->getOption(Memcached::OPT_HASH) == Memcached::HASH_DEFAULT);echo "Pre | Memcached::OPT_PREFIX_KEY), "
";?> `

Результат виконання цього прикладу:

bool(true)
bool(false)
Prefix key is now: widgets

### Дивіться також

- [Memcached::getOption()](memcached.getoption.md) - Отримує
значення Memcached параметра
- [Memcached::setOption()](memcached.setoption.md) - Встановлює
значення параметра для Memcached
- [Memcached Constants](memcached.constants.md)
