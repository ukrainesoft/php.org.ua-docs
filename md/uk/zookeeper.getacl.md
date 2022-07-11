- [« Zookeeper::get](zookeeper.get.md)
- [Zookeeper::getChildren »](zookeeper.getchildren.md)

- [PHP Manual](index.md)
- [Zookeeper](class.zookeeper.md)
- Синхронно отримує ACL, пов'язаний із вузлом

# Zookeeper::getAcl

(PECL zookeeper \>= 0.1.0)

Zookeeper::getAcl — Синхронно отримує ACL, пов'язаний із вузлом

### Опис

public **Zookeeper::getAcl**(string `$path`): array

### Список параметрів

`path`
Ім'я вузла. Виражається як ім'я файлу з косою межею, що розділяє предків
вузла.

### Значення, що повертаються

Повертає масив acl у разі успішного виконання та false у разі
виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли кількість параметрів або
типи неправильні або виходить отримати ACL вузла.

**Застереження**

Починаючи з версії 0.3.0 метод викидає
[ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::getAcl()****

Отримання ACL вузла.

`=?                                       ',  ));$path = '/path/to/newnode';$zookeeper->setAcl($path, $aclArray);$r = $zookeeper->getAcl($path);if ($r) var_dump $r);else  echo 'Помилка';?> `

Результат виконання цього прикладу:

array(1) {
[0]=>
array(3) {
["perms"]=>
int(31)
["scheme"]=>
string(5) "world"
["id"]=>
string(6) "anyone"
}
}

### Дивіться також

- [Zookeeper::create()](zookeeper.create.md) - Створює синхронно
вузол
- [Zookeeper::setAcl()](zookeeper.setacl.md) - Встановлює ACL,
пов'язаний з вузлом синхронно
- [Дозволи ZooKeeper](class.zookeeper.md#zookeeper.class.constants.perms)
- [ZookeeperException](class.zookeeperexception.md)
