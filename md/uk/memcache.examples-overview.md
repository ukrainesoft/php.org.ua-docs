- [« Приклади](memcache.examples.md)
- [Memcache »](class.memcache.md)

- [PHP Manual](index.md)
- [Приклади](memcache.examples.md)
- Базове використання

## Базове використання

**Приклад #1 Приклад використання модуля memcache**

У цьому прикладі відбувається збереження об'єкта в кеші та його наступне
читання. Об'єкти та інші нескалярні типи серіалізуються перед
збереженням, що унеможливлює зберігання ресурсів (наприклад,
ідентифікаторів підключень та ін.) у кеші.

` <?php$memcache = new Memcache;$memcache->connect('localhost', 11211) or die ("Не можу підключитися");$version = $memcache->getVersion(); $version."<br/>
";$tmp_object = new stdClass;$tmp_object->str_attr = 'test';$tmp_object->int_attr = 123;$memcache->set('key', $tmp_object, false, про охран| даних на сервері");echo "Дані збережені в кеші. (час життя даних 10 секунд)<br/>
";$get_result = $memcache->get('key');echo "Дані із кеша:<br/>
";var_dump($get_result);?> `

**Приклад #2 Використання memcache як обробник сесій**

` <?php$session_save_path = "tcp://$host:$port?persistent=1&weight=2&timeout=2&retry_interval=10, ,tcp://$host:$port  ";ini_set('session.save_handler', m ');ini_set('session.save_path', $session_save_path);?> `
