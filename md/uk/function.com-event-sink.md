Зв'язати повідомлення COM з об'єктом PHP

-   [« com\_create\_guid](function.com-create-guid.html)
    
-   [com\_get\_active\_object »](function.com-get-active-object.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Зв'язати повідомлення COM з об'єктом PHP
    

# comeventsink

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

comeventsink — Зв'язати повідомлення COM з об'єктом PHP

### Опис

```methodsynopsis
com_event_sink(variant $variant, object $sink_object, array|string|null $sink_interface = null): bool
```

Зобов'язує об'єкт COM прокидати повідомлення, створені `variant` в об'єкт PHP `sink_object`

Будьте обережні з цією можливістю. Якщо ви робитимете щось схоже на приклад нижче, то це не матиме жодного сенсу під час запуску в контексті веб-сервера.

### Список параметрів

`variant`

`sink_object`

`sink_object` повинен бути екземпляром класу з методами, названими як у вибраному диспетчерському інтерфейсі; ви можете використовувати функцію [com\_print\_typeinfo()](function.com-print-typeinfo.html) для допомоги у генерації шаблону класу.

`sink_interface`

PHP намагатиметься використовувати тип диспетчерського інтерфейсу за промовчанням, як зазначено в бібліотеці типів, пов'язаної з `variant`, але ви можете змінити таку поведінку, поставивши в `sink_interface` ім'я бажаного диспетчерського інтерфейсу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                       |
|--------|------------------------------------------------|
|        | `sink_interface` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад comeventsink**

```php
<?php
class IEEventSinker {
    var $terminated = false;

   function ProgressChange($progress, $progressmax) {
      echo "Прогресс загрузки: $progress / $progressmax\n";
    }

    function DocumentComplete(&$dom, $url) {
      echo "Загрузка $url завершена\n";
    }

    function OnQuit() {
      echo "Quit!\n";
      $this->terminated = true;
    }
}
$ie = new COM("InternetExplorer.Application");
$sink = new IEEventSinker();
com_event_sink($ie, $sink, "DWebBrowserEvents2");
$ie->Visible = true;
$ie->Navigate("http://www.example.org");
while(!$sink->terminated) {
  com_message_pump(4000);
}
$ie = null;
?>
```

### Примітки

**Застереження**

До PHP 8.0.0 виклик [exit()](function.exit.html) з будь-якого оброблювача події не підтримувався і міг призвести до зависання PHP. Це можна обійти, викидаючи виняток з обробника події, перехоплюючи виняток в основному коді та викликаючи звідти [exit()](function.exit.html)

### Дивіться також

-   [com\_print\_typeinfo()](function.com-print-typeinfo.html) - Друкує визначення класу PHP для інтерфейсу, що наслідує IDispatch
-   [com\_message\_pump()](function.com-message-pump.html) - Обробка повідомлень COM, що прийшли не пізніше timeoutms мілісекунд після її запуску