---
navigation:
  - sessionhandler.write.md: '« SessionHandler::write'
  - sessionhandlerinterface.close.md: 'SessionHandlerInterface::close »'
  - index.md: PHP Manual
  - book.session.md: Сесії
title: Клас SessionHandlerInterface
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SessionHandlerInterface

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

## Вступ

**SessionHandlerInterface** - це інтерфейс, який визначає мінімальний прототип для створення користувальницького оброблювача сесії. Для надання користувальницького оброблювача сесії функції [session\_set\_save\_handler()](function.session-set-save-handler.md), Використовуючи її ООП реалізацію, клас повинен реалізовувати цей інтерфейс.

Зауважте, що callback-методи цього класу створені для внутрішніх викликів PHP і не призначені для викликів з вашого коду.

## Огляд інтерфейсів

```classsynopsis

    
     interface SessionHandlerInterface {

    /* Методы */
    
   public close(): bool
public destroy(string $id): bool
public gc(int $max_lifetime): int|false
public open(string $path, string $name): bool
public read(string $id): string|false
public write(string $id, string $data): bool

   }
```

**Приклад #1 Приклад використання** SessionHandlerInterface\*\*\*\*

Наступний приклад реалізує файлову сесію так само, як це реалізовано у внутрішньому обробнику сесії PHP. Цей приклад може бути легко розширений для забезпечення зберігання сесій в базі даних.

Зверніть увагу, що ми використовуємо об'єктно-орієнтовані прототипи з функцією [session\_set\_save\_handler()](function.session-set-save-handler.md) та реєструємо функцію завершення (shutdown) використовуючи один із параметрів цієї функції. Ця дія рекомендується проводити в більшості випадків, коли об'єкти реєструються як обробники сесії.

**Застереження**

Для стислості в цьому прикладі не додано перевірку вхідних даних. Зверніть увагу, що параметр `$id` надається користувачем і обов'язково повинен перевірятися для виключення можливих атак, які використовують, наприклад, проблеми обходу шляху . *Так що в жодному разі не використовуйте цей код у промисловій експлуатації, не додавши відповідних перевірок.*

```php
<?php
class MySessionHandler implements SessionHandlerInterface
{
    private $savePath;
    public function open($savePath, $sessionName): bool
    {
        $this->savePath = $savePath;
        if (!is_dir($this->savePath)) {
            mkdir($this->savePath, 0777);
        }
        return true;
    }
    public function close(): bool
    {
        return true;
    }
    #[\ReturnTypeWillChange]
    public function read($id)
    {
        return (string)@file_get_contents("$this->savePath/sess_$id");
    }
    public function write($id, $data): bool
    {
        return file_put_contents("$this->savePath/sess_$id", $data) === false ? false : true;
    }
    public function destroy($id): bool
    {
        $file = "$this->savePath/sess_$id";
        if (file_exists($file)) {
            unlink($file);
        }
        return true;
    }
    #[\ReturnTypeWillChange]
    public function gc($maxlifetime)
    {
        foreach (glob("$this->savePath/sess_*") as $file) {
            if (filemtime($file) + $maxlifetime < time() && file_exists($file)) {
                unlink($file);
            }
        }
        return true;
    }
}
$handler = new MySessionHandler();
session_set_save_handler($handler, true);
session_start();

// продолжаем работать с переменными сессии, устанавливая или читая их значение из $_SESSION
```

## Зміст

-   [SessionHandlerInterface::close](sessionhandlerinterface.close.md) \- Закриває сесію
-   [SessionHandlerInterface::destroy](sessionhandlerinterface.destroy.md) \- Знищує сесію
-   [SessionHandlerInterface::gc](sessionhandlerinterface.gc.md) \- Очищає старі сесії
-   [SessionHandlerInterface::open](sessionhandlerinterface.open.md) \- Ініціалізує сесію
-   [SessionHandlerInterface::read](sessionhandlerinterface.read.md)— Читає дані сесії
-   [SessionHandlerInterface::write](sessionhandlerinterface.write.md)— Записати дані сесії
