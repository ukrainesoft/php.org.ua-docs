Розбір та лексування

-   [« CommonMark\\Render\\XML](function.commonmark-render-xml.html)
    
-   [Введение »](intro.parle.html)
    
-   [PHP Manual](index.html)
    
-   [Обработка текста](refs.basic.text.html)
    
-   Розбір та лексування
    

# Розбір та лексування

-   [Введение](intro.parle.html)
-   [Установка и настройка](parle.setup.html)
    -   [Требования](parle.requirements.html)
    -   [Установка](parle.installation.html)
-   [Предопределённые константы](parle.constants.html)
-   [Сопоставление с шаблоном](parle.pattern.matching.html) — Зіставлення із шаблоном Parle
    -   [Представления символов](parle.regex.chars.html)
    -   [Классы символов](parle.regex.charclass.html)
    -   [Классы символов Unicode](parle.regex.unicodecharclass.html)
    -   [Чередование и повторение](parle.regex.alternation.html)
    -   [Якоря](parle.regex.anchors.html)
    -   [Группировка](parle.regex.grouping.html)
-   [Примеры](parle.examples.html)
    -   [Примеры использования лексера](parle.examples.lexer.html)
    -   [Пример использования парсера](parle.examples.parser.html)
-   [Parle\\Lexer](class.parle-lexer.html) - Клас ParleLexer
    -   [Parle\\Lexer::advance](parle-lexer.advance.html) - Обробляє таке правило лексера
    -   [Parle\\Lexer::build](parle-lexer.build.html) - Завершує набір правил лексера
    -   [Parle\\Lexer::callout](parle-lexer.callout.html) - Визначає callback-функцію токена
    -   [Parle\\Lexer::consume](parle-lexer.consume.html) - Передає дані на обробку
    -   [Parle\\Lexer::dump](parle-lexer.dump.html) - Виводить стан пристрою
    -   [Parle\\Lexer::getToken](parle-lexer.gettoken.html) — Отримує поточний токен
    -   [Parle\\Lexer::insertMacro](parle-lexer.insertmacro.html) — Вставляє макрос регулярного виразу
    -   [Parle\\Lexer::push](parle-lexer.push.html) - Додає правило лексера
    -   [Parle\\Lexer::reset](parle-lexer.reset.html) - скидає лексер
-   [Parle\\RLexer](class.parle-rlexer.html) - Клас ParleRLexer
    -   [Parle\\RLexer::advance](parle-rlexer.advance.html) - Обробка наступного правила лексера
    -   [Parle\\RLexer::build](parle-rlexer.build.html) - Завершує набір правил лексера
    -   [Parle\\RLexer::callout](parle-rlexer.callout.html) - Визначає callback-функцію токена
    -   [Parle\\RLexer::consume](parle-rlexer.consume.html) — Передає дані для обробки
    -   [Parle\\RLexer::dump](parle-rlexer.dump.html) — Вивантажує стан пристрою
    -   [Parle\\RLexer::getToken](parle-rlexer.gettoken.html) - в
    -   [Parle\\RLexer::insertMacro](parle-rlexer.insertmacro.html) — Вставляє макрос регулярного виразу
    -   [Parle\\RLexer::push](parle-rlexer.push.html) - Додає правило лексера
    -   [Parle\\RLexer::pushState](parle-rlexer.pushstate.html) - Просуває новий початковий стан
    -   [Parle\\RLexer::reset](parle-rlexer.reset.html) - скидає лексер
-   [Parle\\Parser](class.parle-parser.html) - Клас ParleParser
    -   [Parle\\Parser::advance](parle-parser.advance.html) - Обробляє наступне правило парсера
    -   [Parle\\Parser::build](parle-parser.build.html) - Завершує граматичні правила
    -   [Parle\\Parser::consume](parle-parser.consume.html) — Використовує дані для обробки
    -   [Parle\\Parser::dump](parle-parser.dump.html) - Виводить граматику
    -   [Parle\\Parser::errorInfo](parle-parser.errorinfo.html) — Отримує інформацію про помилку
    -   [Parle\\Parser::left](parle-parser.left.html) - Оголошує токен з лівою асоціативністю
    -   [Parle\\Parser::nonassoc](parle-parser.nonassoc.html) - Оголошує токен без асоціативності
    -   [Parle\\Parser::precedence](parle-parser.precedence.html) — Оголошує правило пріоритету
    -   [Parle\\Parser::push](parle-parser.push.html) — Додає граматичне правило
    -   [Parle\\Parser::reset](parle-parser.reset.html) — скидає стан парсера
    -   [Parle\\Parser::right](parle-parser.right.html) — Оголошує токен із правою асоціативністю
    -   [Parle\\Parser::sigil](parle-parser.sigil.html) — Витягує частину збігу за правилом
    -   [Parle\\Parser::token](parle-parser.token.html) - Оголошує токен
    -   [Parle\\Parser::tokenId](parle-parser.tokenid.html) — Отримує ідентифікатор токена
    -   [Parle\\Parser::trace](parle-parser.trace.html) — Слідкує за роботою парсера
    -   [Parle\\Parser::validate](parle-parser.validate.html) - Перевіряє вхідні дані
-   [Parle\\RParser](class.parle-rparser.html) - Клас ParleRParser
    -   [Parle\\RParser::advance](parle-rparser.advance.html) - Обробка наступного правила парсера
    -   [Parle\\RParser::build](parle-rparser.build.html) - Завершує граматичні правила
    -   [Parle\\RParser::consume](parle-rparser.consume.html) — Використовувати дані для обробки
    -   [Parle\\RParser::dump](parle-rparser.dump.html) - Виводить граматику
    -   [Parle\\RParser::errorInfo](parle-rparser.errorinfo.html) — Отримує інформацію про помилку
    -   [Parle\\RParser::left](parle-rparser.left.html) - Оголошує токен з лівою асоціативністю
    -   [Parle\\RParser::nonassoc](parle-rparser.nonassoc.html) - Оголошує токен без асоціативності
    -   [Parle\\RParser::precedence](parle-rparser.precedence.html) — Оголошує правило пріоритету
    -   [Parle\\RParser::push](parle-rparser.push.html) — Додає граматичне правило
    -   [Parle\\RParser::reset](parle-rparser.reset.html) — скидає стан парсера
    -   [Parle\\RParser::right](parle-rparser.right.html) — Оголошує токен із правою асоціативністю
    -   [Parle\\RParser::sigil](parle-rparser.sigil.html) — Витягує збігаючу частину за правилом
    -   [Parle\\RParser::token](parle-rparser.token.html) - Оголошує токен
    -   [Parle\\RParser::tokenId](parle-rparser.tokenid.html) — Отримує ідентифікатор токена
    -   [Parle\\RParser::trace](parle-rparser.trace.html) — Слідкує за роботою парсера
    -   [Parle\\RParser::validate](parle-rparser.validate.html) - Перевіряє вхідні дані
-   [Parle\\Stack](class.parle-stack.html) - Клас ParleStack
    -   [Parle\\Stack::pop](parle-stack.pop.html) — Витягує предмет із стеку
    -   [Parle\\Stack::push](parle-stack.push.html) — Поміщає елемент у стек
-   [Parle\\Token](class.parle-token.html) - Клас ParleToken
-   [Parle\\ErrorInfo](class.parle-errorinfo.html) - Клас ParleErrorInfo
-   [Parle\\LexerException](class.parle-lexerexception.html) - Клас ParleLexerException
-   [Parle\\ParserException](class.parle-parserexception.html) - Клас ParleParserException