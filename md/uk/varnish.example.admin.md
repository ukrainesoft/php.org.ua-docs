- [« Приклади](varnish.examples.md)
- [Просте використання VarnishStat »](varnish.example.stat.md)

- [PHP Manual](index.md)
- [Приклади](varnish.examples.md)
- Просте використання VarnishAdmin

## Просте використання VarnishAdmin

Цей приклад ілюструє просте використання функціональності
заборони

**Приклад #1 Заборонити URL**

` <?php$args = array(    VARNISH_CONFIG_HOST    => "::1",    VARNISH_CONFIG_PORT    => 6082,    VARNISH_CONFIG_SECRET  => "5174826b-8595-4958-aa7a-0609632ad7ca",    VARNISH_CONFIG_TIMEOUT => 300,);$va = new VarnishAdmin ($args);try { {   if(!$va->connect()) {        throw new VarnishException("Невдале підключення
");    }} catch (VarnishException $e) {    echo $e->getMessage();    exit(3);}try {    if(!
");    }} catch (VarnishException $e) {    echo $e->getMessage();    exit(3);}try {    $status = $va| ;   if (VARNISH_STATUS_OK != $status) {       throw new VarnishException("Метод ban вернув статус $status
");    }} catch (VarnishException $e) {    echo $e->getMessage();    exit(3);}exit(0);?> `
