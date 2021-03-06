- [« Yaf_Dispatcher::setRequest](yaf-dispatcher.setrequest.md)
- [Yaf_Dispatcher::throwException »](yaf-dispatcher.throwexception.md)

- [PHP Manual](index.md)
- [Yaf_Dispatcher](class.yaf-dispatcher.md)
- Встановлює користувальницький механізм відображення

# Yaf_Dispatcher::setView

(Yaf \>=1.0.0)

Yaf_Dispatcher::setView — Встановлює механізм користувача
відображення

### Опис

public
**Yaf_Dispatcher::setView**([Yaf_View_Interface](class.yaf-view-interface.md)
`$view`): [Yaf_Dispatcher](class.yaf-dispatcher.md)

Метод надає рішення, якщо ви хочете використати власний
механізм відображення замість
[Yaf_View_Simple](class.yaf-view-simple.md).

### Список параметрів

`view`
Примірник [Yaf_View_Interface](class.yaf-view-interface.md)

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **двигуна користувача
відображення()****

`<?phprequire "/path/to/smarty/Smarty.class.php";class Smarty_Adapter implements Yaf_View_Interface{    /**    * Smarty object                                        /**     * Конструктор     *     * @param string $tmplPath     * @param array $extraParams     * @return void     */    public function __construct($tmplPath = null, $extraParams = array()) {        $this->_smarty = new Smarty; if (null !== $tmplPath) {            $this->setScriptPath($tmplPath); }        foreach ($extraParams as $key => $value) {            $this->_smarty->$key = $value; }    }    /**     * Задайте шляху к шаблонам     *     * @param string $path запропонувати| * @return void     */    public function setScriptPath($path)   {        if (is_readable($path)) _ return; }        throw new Exception('Invalid path provided'); }    /**     * Призначте змінну шаблону     *     * @param string $key Ім'я змінною mi| * @return void     */    public function __set($key, $val)   {{       $this->_smarty->assign($key, $val); }    /**     * Разрешает тестирование с empty() и isset()     *     * @param string $key     * @return boolean     */    public function __isset($key)    {        return (null !== $this->_smarty->get_template_vars ($ key)); }    /**     * Разрешает unset() для свойств объекта     *     * @param string $key     * @return void     */    public function __unset($key)    {        $this->_smarty->clear_assign($key); }    /**     * Призначте змінні шаблону     *     * Дозволяє встановити конкретний ключ| *     * @see __set()     * @param string|array $spec Стратегия присваивания (ключ или массив пар ключ => значение)     * @param mixed $value (Optional) При присвоении именованной переменной используйте её как значение. * @return void     */    public function assign($spec, $value = null) {                                     Я — (                             Яляхах:) return; }        $this->_smarty->assign($spec, $value); }    /**     * Очистить все присвоенные переменные     *     * Очищает все переменные, назначенные Yaf_View, либо через     * {@link assign()} или перезагрузку свойства     * ({@link __get()}/{@link __set()}). *     * @return void     */    public function clearVars() {       $this->_smarty->clear_all_assign(); }    /**     * Обробляє шаблон і повертає результат. *     * @param string $name Шаблон для обробки. * @return string Висновок. */    public function render($name, $value = NULL) {       return $this->_smarty->fetch($name); }    public function display($name, $value = NULL) {       echo $this->_smarty->fetch($name); }}?> `

**Приклад #2 Приклад використання **Yaf_Dispatcher::setView()****

` <?phpclass Bootstrap extends Yaf_Bootstrap_Abstract {    /**     * конфигурация для smarty в конфигурации:     *     * smarty.left_delimiter   = "{{"     * smarty.right_delimiter  = "}}"     * smarty.template_dir     = APPLICATION_PATH "/views/scripts/" * smarty.compile_dir      = APPLICATION_PATH "/views/templates_c/"     * smarty.cache_dir        = APPLICATION_PATH "/views/templates_d/"     *     */    public function _initConfig() {        $config = Yaf_Application::app()->getConfig(); Yaf_Registry::set("config", $config); }    public function _initLocalName() {   | }    public function _initSmarty(Yaf_Dispatcher $dispatcher) {       $smarty = new Smarty_Adapter(null, Yaf_Registry::get("config")->get" $dispatcher->setView($smarty); /* тепер механізм відображення Smarty стал механізмом відображення за замовчуванням для Yaf */    }}?> `

### Дивіться також

- [Yaf_View_Interface](class.yaf-view-interface.md)
- [Yaf_View_Simple](class.yaf-view-simple.md)
