Клас com

-   [« Массивы и свойства COM в стиле массивов](com.examples.arrays.html)
    
-   [com::\_\_construct »](com.construct.html)
    
-   [PHP Manual](index.html)
    
-   [COM](book.com.html)
    
-   Клас com
    

# Клас com

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

## Вступ

Клас com дозволяє створювати екземпляри OLE-сумісного COM-об'єкта, викликати його методи та отримувати доступ до його властивостей.

## Огляд класів

```synopsis

     
    

    
     
      class com
     

    
     extends
      variant
    

     {

    /* Методы */
    
   public __construct(    string $module_name,    array|string|null $server_name = null,    int $codepage = CP_ACP,    string $typelib = "")

   }
```

## Перевантажені методи

Об'єкти, що повертаються, є перевантаженими, тобто PHP не бачить будь-яких фіксованих методів, як це відбувається зі звичайними класами. Замість цієї властивості та доступ до методів передається через COM.

PHP автоматично визначає методи, які звертаються до властивостей посилань і автоматично перетворять стандартні змінні PHP у вигляд, який можна передавати за посиланням. Це означає, що ви можете викликати методи, не вносячи будь-яких доповнень до свого коду.

## Приклади використання com

**Приклад #1 Перший приклад**

```php
<?php
// запускаем word
$word = new com("word.application") or die("Невозможно создать экземпляр Word");
echo "Загружен Word, версия {$word->Version}\n";

//делаем его активным окном
$word->Visible = 1;

//открываем пустой документ
$word->Documents->Add();

//Что то с ним делаем
$word->Selection->TypeText("Это проверка...");
$word->Documents[1]->SaveAs("Бесполезный тест.doc");

//закрываем word
$word->Quit();

//высвобождаем ресурсы объекта
$word = null;
?>
```

**Приклад #2 Другий приклад**

```php
<?php

$conn = new com("ADODB.Connection") or die("Cannot start ADO");
$conn->Open("Provider=SQLOLEDB; Data Source=localhost;
Initial Catalog=database; User ID=user; Password=password");

$rs = $conn->Execute("SELECT * FROM sometable");    // Набор записей

$num_columns = $rs->Fields->Count();
echo $num_columns . "\n";

for ($i=0; $i < $num_columns; $i++) {
    $fld[$i] = $rs->Fields($i);
}

$rowcount = 0;
while (!$rs->EOF) {
    for ($i=0; $i < $num_columns; $i++) {
        echo $fld[$i]->value . "\t";
    }
    echo "\n";
    $rowcount++;            // увеличиваем счётчик строк
    $rs->MoveNext();
}

$rs->Close();
$conn->Close();

$rs = null;
$conn = null;

?>
```

## Зміст

-   [com::\_\_construct](com.construct.html) - Конструктор класу com