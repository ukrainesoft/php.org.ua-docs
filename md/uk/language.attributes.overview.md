Введення в атрибути

-   [« Атрибути](language.attributes.md)
    
-   [Синтаксис атрибутів »](language.attributes.syntax.md)
    
-   [PHP Manual](index.md)
    
-   [Атрибути](language.attributes.md)
    
-   Введення в атрибути
    

## Введення в атрибути

(PHP 8)

Атрибути пропонують можливість додавати структуровані, машиночитані метадані для наступних декларацій у коді: класи, методи, функції, параметри, властивості та константи класу. Прив'язані метадані можна отримати під час виконання, використовуючи [Reflection API](book.reflection.md). Таким чином, атрибути можна розглядати як мову конфігурації, вбудовану безпосередньо в код.

За допомогою атрибутів можна розділити абстрактну реалізацію будь-якої функціональності та особливості її використання у коді. У певному сенсі це можна порівняти з розподілом інтерфейсу та його реалізацій. Але інтерфейси та реалізації – це про код, а атрибути – про додавання додаткової інформації та конфігурацію. Інтерфейси можуть бути реалізовані тільки класами, тоді як атрибути також застосовні для методів, функцій, параметрів, властивостей і констант класів. Таким чином, вони є набагато більш гнучкий механізм, ніж інтерфейси.

Розберемо використання атрибутів на простому прикладі реалізації опціональних методів для інтерфейсу. Припустимо, що інтерфейс `ActionHandler` визначає якусь операцію у додатку. Одні реалізації цього інтерфейсу вимагають попереднього налаштування, а інші - ні. І замість того, щоб вносити до інтерфейсу `ActionHandler` додатковий метод `setUp()`, Що для частини реалізацій буде порожнім, можна використовувати атрибут. Однією з переваг цього підходу є те, що ми можемо використовувати атрибут кілька разів.

**Приклад #1 Реалізація опціональних методів інтерфейсу за допомогою атрибутів**

```php
<?php
interface ActionHandler
{
    public function execute();
}

#[Attribute]
class SetUp {}

class CopyFile implements ActionHandler
{
    public string $fileName;
    public string $targetDirectory;

    #[SetUp]
    public function fileExists()
    {
        if (!file_exists($this->fileName)) {
            throw new RuntimeException("File does not exist");
        }
    }

    #[SetUp]
    public function targetDirectoryExists()
    {
        if (!file_exists($this->targetDirectory)) {
            mkdir($this->targetDirectory);
        } elseif (!is_dir($this->targetDirectory)) {
            throw new RuntimeException("Target directory $this->targetDirectory is not a directory");
        }
    }

    public function execute()
    {
        copy($this->fileName, $this->targetDirectory . '/' . basename($this->fileName));
    }
}

function executeAction(ActionHandler $actionHandler)
{
    $reflection = new ReflectionObject($actionHandler);

    foreach ($reflection->getMethods() as $method) {
        $attributes = $method->getAttributes(SetUp::class);

        if (count($attributes) > 0) {
            $methodName = $method->getName();

            $actionHandler->$methodName();
        }
    }

    $actionHandler->execute();
}

$copyAction = new CopyFile();
$copyAction->fileName = "/tmp/foo.jpg";
$copyAction->targetDirectory = "/home/user";

executeAction($copyAction);
```