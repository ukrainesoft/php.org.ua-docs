- [« Приклади](tidy.examples.md)
- [tidy »](class.tidy.md)

- [PHP Manual](index.md)
- [Приклади](tidy.examples.md)
- Приклад використання Tidy

## Приклад використання Tidy

Простий приклад демонструє базові можливості використання Tidy.

**Приклад #1 Базові можливості використання Tidy**

` <?phpob_start();?><html>a html document</html><?php$html = ob_get_clean();// Установка конфигурации$config = array(           'indent'         => true,           'output-xhtml' => true,           'wrap'            => 200);// Tidy$tidy = new tidy;$tidy->parseString($>| tidy;?> `
