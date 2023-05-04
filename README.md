# Справка по Selenium.
В основном как веб-драйвер использую хром.

## Инициализация драйвера:
using OpenQA;<br>
using OpenQA.Selenium;<br>
using OpenQA.Selenium.Chrome;<br>

IWebDriver web = new ChromeDriver();

## Открыть ссылку:
web.Navigate().GoToUrl(link);

## Открыть ссылку в новом окне:
web.SwitchTo().NewWindow(WindowType.Tab);<br>
web.Navigate().GoToUrl(link);<br>

## Явное ожидание:
Thread.Sleep(7000);<br>
//В милисекундах

## Найти элемент на текущей странице:
web.FindElement(By.Xpath(""));<br>
//Я использую Xpath(удобно через расширение в браузере смотреть), в кавычках пишется путь к элементу странице в виде XML - //p[@class='wa-overview__title']



