- [« Swoole\Event::write](swoole-event.write.md)
- [Swoole\Http\Client »](class.swoole-http-client.md)

- [PHP Manual](index.md)
- [Swoole](book.swoole.md)
- Клас Swoole\Exception

# Клас Swoole\Exception

(PECL swoole \>= 1.9.0)

## Вступ

## Огляд класів

class **Swoole\Exception** extends [Exception](class.exception.md)
implements [Throwable](class.throwable.md) {

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

}
