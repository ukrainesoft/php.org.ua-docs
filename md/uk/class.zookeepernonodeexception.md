- [« ZookeeperMarshallingException](class.zookeepermarshallingexception.md)
- [ZookeeperOperationTimeoutException »](class.zookeeperoperationtimeoutexception.md)

- [PHP Manual](index.md)
- [ZooKeeper](book.zookeeper.md)
- Клас ZookeeperNoNodeException

# Клас ZookeeperNoNodeException

(PECL zookeeper \>= 0.3.0)

## Вступ

Клас обробки винятків ZooKeeper (у разі відсутності вузла).

## Огляд класів

class **ZookeeperNoNodeException** extends
[ZookeeperException](class.zookeeperexception.md) {

/\* Наслідувані властивості \*/

protected string `$message` = "";

private string `$string` = "";

protected int `$code`;

protected string `$file` = "";

protected int `$line`;

private array `$trace` = [];
 private ?[Throwable](class.throwable.md) `$previous` = null;

/\* Наслідувані методи \*/

final public [Exception::getMessage](exception.getmessage.md)():
string

final public [Exception::getPrevious](exception.getprevious.md)():
?[Throwable](class.throwable.md)

final public [Exception::getCode](exception.getcode.md)(): int

final public [Exception::getFile](exception.getfile.md)(): string

final public [Exception::getLine](exception.getline.md)(): int

final public [Exception::getTrace](exception.gettrace.md)(): array

final public
[Exception::getTraceAsString](exception.gettraceasstring.md)(): string

public [Exception::\_\_toString](exception.tostring.md)(): string

private [Exception::\_\_clone](exception.clone.md)(): void

}
