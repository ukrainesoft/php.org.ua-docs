---
navigation:
  - language.attributes.md: « Атрибути
  - language.attributes.syntax.md: Синтаксис атрибутів »
  - index.md: PHP Manual
  - language.attributes.md: Атрибути
title: Введення в атрибути
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Введення в атрибути

(PHP 8)

Атрибути — це структуровані машиночитані метадані, оголошені кодом. Метою атрибутів можуть бути: класи (включаючи анонімні), методи, функції, параметри, властивості та константи класу. Потім описані атрибутами метадані можна проаналізувати під час виконання засобами [Reflection API](book.reflection.md). Тому атрибути можна розглядати як вбудовану в код мову конфігурації.

Атрибути поділяють загальну та специфічну поведінку сутностей у додатку. В якомусь сенсі це схоже на інтерфейс із його реалізаціями. Але інтерфейси та реалізації – це про код, а атрибути – про додавання додаткової інформації та конфігурацію. Інтерфейси можуть реалізовуватися лише класами, тоді як атрибути можна націлювати на методи, функції, параметри, властивості та константи класів. Тому атрибути — значно більш гнучкий механізм, ніж інтерфейси.

Простий приклад заміни інтерфейсу з необов'язковими методами коду з атрибутами. Припустимо, інтерфейс `ActionHandler` описує у додатку операцію, до виконання якої одним реалізаціям потрібна попередня настройка, а іншим — ні. І замість внесення до інтерфейсу `ActionHandler`дополнительного метода`setUp()`, Що для частини реалізацій буде порожнім, можна використовувати атрибут. Однією з переваг цього підходу є те, що ми можемо використати атрибут кілька разів.

**Приклад #1 Реалізація опціональних методів інтерфейсу за допомогою атрибутів**

```php
<?php
interface ActionHandler
{
    public function execute();
}

#[Attribute]
class SetUp {}

class CopyFile implements ActionHandler
{
    public string $fileName;
    public string $targetDirectory;

    #[SetUp]
    public function fileExists()
    {
        if (!file_exists($this->fileName)) {
            throw new RuntimeException("File does not exist");
        }
    }

    #[SetUp]
    public function targetDirectoryExists()
    {
        if (!file_exists($this->targetDirectory)) {
            mkdir($this->targetDirectory);
        } elseif (!is_dir($this->targetDirectory)) {
            throw new RuntimeException("Target directory $this->targetDirectory is not a directory");
        }
    }

    public function execute()
    {
        copy($this->fileName, $this->targetDirectory . '/' . basename($this->fileName));
    }
}

function executeAction(ActionHandler $actionHandler)
{
    $reflection = new ReflectionObject($actionHandler);

    foreach ($reflection->getMethods() as $method) {
        $attributes = $method->getAttributes(SetUp::class);

        if (count($attributes) > 0) {
            $methodName = $method->getName();

            $actionHandler->$methodName();
        }
    }

    $actionHandler->execute();
}

$copyAction = new CopyFile();
$copyAction->fileName = "/tmp/foo.jpg";
$copyAction->targetDirectory = "/home/user";

executeAction($copyAction);
```
