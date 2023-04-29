# Справка по Selenium.
В основном как веб-драйвер использую хром.

## Инициализация драйвера:
using OpenQA;
using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;

IWebDriver web = new ChromeDriver();



## Новое окно:
web.SwitchTo().NewWindow(WindowType.Tab);
