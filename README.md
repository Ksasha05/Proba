# Справка по Selenium.
В основном как веб-драйвер использую хром.

## Инициализация драйвера:
using OpenQA;<br>
using OpenQA.Selenium;<br>
using OpenQA.Selenium.Chrome;<br>

IWebDriver web = new ChromeDriver();



## Новое окно:
web.SwitchTo().NewWindow(WindowType.Tab);
