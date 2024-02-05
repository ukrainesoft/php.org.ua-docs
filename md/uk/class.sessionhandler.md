---
navigation:
  - function.session-write-close.md: « session\_write\_close
  - sessionhandler.close.md: 'SessionHandler::close »'
  - index.md: PHP Manual
  - book.session.md: Сесії
title: Клас SessionHandler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SessionHandler

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

**SessionHandler** це спеціальний клас, який може використовуватись для доповнення внутрішнього оброблювача сесій PHP шляхом створення дочірніх класів від цього. Існує сім методів, які є обгортками над сімома внутрішніми обробниками зберігання даних сесії (`open` `close` `read` `write` `destroy` `gc`и`create_sid`). За умовчанням цей клас обертає всі внутрішні обробники сесії, визначені в опції конфігурації [session.save\_handler](session.configuration.md#ini.session.save-handler). За замовчуванням ця опція має значення `files`Другие внутренние обработчики сессий предоставляются PHP-модулями, такими как SQLite (`sqlite`), Memcache (`memcache`) та Memcached (`memcached`

Екземпляр класу **SessionHandler** може встановлюватися як обробник сесії за допомогою виклику функції [session\_set\_save\_handler()](function.session-set-save-handler.md). У цьому випадку він стане обгорткою існуючого внутрішнього оброблювача. Класи, що розширюють **SessionHandler** дозволять перевизначити методи оброблювача сесії або перехопити/відфільтрувати їх шляхом виклику батьківських методів-оберток внутрішнього оброблювача сесій PHP.

Це дозволить вам, наприклад, перехопити методи `read`и`write` для шифрування/дешифрування даних сесії та передачі результату батьківському класу та від нього. Або, наприклад, ви можете повністю перевизначити такий метод як callback-функція збирача сміття (`gc`

Так как**SessionHandler** є обгорткою над стандартним внутрішнім обробником сесії, то приклад, наведений вище про шифрування даних може бути застосований до будь-якого внутрішнього оброблювача сесії навіть без розуміння внутрішнього пристрою процесу сесії.

Для використання цього класу, по-перше, встановіть обробник, який ви хочете доповнити, використовуючи [session.save\_handler](session.configuration.md#ini.session.save-handler). Далі передайте екземпляр класу **SessionHandler** або одного з класів, що розширюють його функції [session\_set\_save\_handler()](function.session-set-save-handler.md)

Зверніть увагу, що callback-методи цього класу призначені для внутрішнього виклику PHP і не призначені для виклику з коду простору користувача. Значення, що повертаються однаково обробляються всередині PHP. Додаткову інформацію про роботу із сесією можна дізнатися з опису функції [session\_set\_save\_handler()](function.session-set-save-handler.md)

## Огляд класів

```classsynopsis

    
     class SessionHandler
    

    
     implements
      SessionHandlerInterface,

     SessionIdInterface {

    /* Методы */
    
   public close(): bool
public create_sid(): string
public destroy(string $id): bool
public gc(int $max_lifetime): int|false
public open(string $path, string $name): bool
public read(string $id): string|false
public write(string $id, string $data): bool

   }
```

**Увага**

Цей клас призначений для розширення поточного внутрішнього оброблювача сесії PHP. При цьому, якщо вам потрібно написати власний обробник, необхідно написати власну реалізацію інтерфейсу [SessionHandlerInterface](class.sessionhandlerinterface.md)вместо расширения класса**SessionHandler**

**Приклад #1 Использование**SessionHandler\*\* для того, щоб додати шифрування даних до внутрішнього оброблювача сесій PHP.\*\*

```php
<?php

 /**
  * расшифровать данные, используя алгоритм AES 256
  *
  * @param data $edata
  * @param string $password
  * @return расшифрованные данные
  */
function decrypt($edata, $password) {
    $data = base64_decode($edata);
    $salt = substr($data, 0, 16);
    $ct = substr($data, 16);

    $rounds = 3; // зависит от длины ключа
    $data00 = $password.$salt;
    $hash = array();
    $hash[0] = hash('sha256', $data00, true);
    $result = $hash[0];
    for ($i = 1; $i < $rounds; $i++) {
        $hash[$i] = hash('sha256', $hash[$i - 1].$data00, true);
        $result .= $hash[$i];
    }
    $key = substr($result, 0, 32);
    $iv  = substr($result, 32,16);

    return openssl_decrypt($ct, 'AES-256-CBC', $key, true, $iv);
  }

/**
 * зашифровать данные алгоритмом AES 256
 *
 * @param data $data
 * @param string $password
 * @return base64 зашифрованные данные
 */
function encrypt($data, $password) {
    // Генерация криптографически безопасной случайной соли с помощью функции random_bytes()
    $salt = random_bytes(16);

    $salted = '';
    $dx = '';
    // Ключ соли (32) и вектор инициализации (16) = 48
    while (strlen($salted) < 48) {
      $dx = hash('sha256', $dx.$password.$salt, true);
      $salted .= $dx;
    }

    $key = substr($salted, 0, 32);
    $iv  = substr($salted, 32,16);

    $encrypted_data = openssl_encrypt($data, 'AES-256-CBC', $key, true, $iv);
    return base64_encode($salt . $encrypted_data);
}

class EncryptedSessionHandler extends SessionHandler
{
    private $key;

    public function __construct($key)
    {
        $this->key = $key;
    }

    public function read($id)
    {
        $data = parent::read($id);

        if (!$data) {
            return "";
        } else {
            return decrypt($data, $this->key);
        }
    }

    public function write($id, $data)
    {
        $data = encrypt($data, $this->key);

        return parent::write($id, $data);
    }
}

// Здесь мы перехватываем встроенный обработчик 'files', но можно использовать любой другой
// обработчик, наПриклад 'sqlite', 'memcache' или 'memcached',
// которые предоставлены модулями PHP.
ini_set('session.save_handler', 'files');

$key = 'secret_string';
$handler = new EncryptedSessionHandler($key);
session_set_save_handler($handler, true);
session_start();

// устанавливаем и получаем значения из $_SESSION
```

> **Зауваження** :
> 
> Так як методи цього класу призначені для внутрішніх викликів з PHP, як частина нормального процесу роботи сесій, виклики батьківських методів із дочірнього класу (іншими словами "рідних" обробників) буде повертати **`false`** доти, доки сесія не буде запущена (автоматично або прямим викликом [session\_start()](function.session-start.md)). Це важливий момент для розуміння, особливо під час тестування, де методи класу можуть бути викликані вручну.

## Зміст

-   [SessionHandler::close](sessionhandler.close.md) \- Закриває сесію
-   [SessionHandler::create\_sid](sessionhandler.create-sid.md)— Повертає новий ідентифікатор сесії
-   [SessionHandler::destroy](sessionhandler.destroy.md) \- Знищує сесію
-   [SessionHandler::gc](sessionhandler.gc.md) \- Очищає старі сесії
-   [SessionHandler::open](sessionhandler.open.md) \- Ініціалізує сесію
-   [SessionHandler::read](sessionhandler.read.md)— Зчитує дані сесії
-   [SessionHandler::write](sessionhandler.write.md)— Записує дані сесії
