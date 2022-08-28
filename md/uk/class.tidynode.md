Клас tidyNode

-   [« tidy::root](tidy.root.html)
    
-   [tidyNode::\_\_construct »](tidynode.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Tidy](book.tidy.html)
    
-   Клас tidyNode
    

# Клас [tidyNode](class.tidynode.html)

(PHP 5, PHP 7, PHP 8)

## Вступ

У HTML-коді не в HTML-файлі, як виявлено тиді.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class tidyNode
     
     {

    /* Свойства */
    
     public
     readonly
     string
      $value;

    public
     readonly
     string
      $name;

    public
     readonly
     int
      $type;

    public
     readonly
     int
      $line;

    public
     readonly
     int
      $column;

    public
     readonly
     bool
      $proprietary;

    public
     readonly
     ?int
      $id;

    public
     readonly
     ?array
      $attribute;

    public
     readonly
     ?array
      $child;


    /* Методы */
    
   private __construct()

    public getParent(): ?tidyNode
public hasChildren(): bool
public hasSiblings(): bool
public isAsp(): bool
public isComment(): bool
public isHtml(): bool
public isJste(): bool
public isPhp(): bool
public isText(): bool

   }
```

## Властивості

value

HTML-подання вузла, включаючи навколишні теги.

name

Назва HTML-вузла

type

Тип тега (одна з [констант](tidy.constants.html#tidy.constants.nodetype), описаних вище, наприклад **`TIDY_NODETYPE_PHP`**

line

Номер рядка, на якому розташований тег у файлі

column

Номер стовпця, на якому розташований тег у файлі

proprietary

Ознака пропрієтарності тега

ід

Ідентифікатор тега (одна з [констант](tidy.constants.html#tidy.constants.tag), описаних вище, наприклад **`TIDY_TAG_FRAME`**

attribute

Масив рядків, що представляють імена атрибутів (як ключі) поточного вузла.

child

Масив, що складається з екземплярів **tidyNode**представляє дітей поточного вузла.

## Зміст

-   [tidyNode::\_\_construct](tidynode.construct.html) — Приватний конструктор, який унеможливлює пряме створення об'єкта
-   [tidyNode::getParent](tidynode.getparent.html) - Повертає батьківський вузол поточного вузла
-   [tidyNode::hasChildren](tidynode.haschildren.html) - Перевіряє існування нащадків біля вузла
-   [tidyNode::hasSiblings](tidynode.hassiblings.html) - Перевіряє існування сусідніх вузлів
-   [tidyNode::isAsp](tidynode.isasp.html) — Перевіряє поточний вузол на відповідність ASP
-   [tidyNode::isComment](tidynode.iscomment.html) — Перевіряє, чи є вузол коментарем
-   [tidyNode::isHtml](tidynode.ishtml.html) — Перевіряє, чи є вузол вузлом елемента
-   [tidyNode::isJste](tidynode.isjste.html) — Перевіряє поточний вузол на відповідність JSTE
-   [tidyNode::isPhp](tidynode.isphp.html) — Перевіряє, чи є поточний вузол PHP-кодом
-   [tidyNode::isText](tidynode.istext.html) — Перевіряє, чи поточний вузол є звичайним текстом (не розміткою)