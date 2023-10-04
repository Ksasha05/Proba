# Справка по Selenium. (C#)
В основном как веб-драйвер использую Edge.

## Инициализация драйвера:
using OpenQA;<br>
using OpenQA.Selenium;<br>
using OpenQA.Selenium.Edge;<br>

IWebDriver web = new EdgeDriver();

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
//Я использую Xpath(удобно через расширение в браузере смотреть), в кавычках пишется путь к элементу странице<br>
в виде XML - //p[@class='wa-overview__title']

## Нажатие на элемент:
web.FindElement(By.Xpath("")).Click();<br>

## Выбрать текст элемента:
string text = web.FindElement(By.Xpath("")).Text;<br>

## Вставить значение в элемент(например в поле ввода):
string text = "text";<br>
web.FindElement(By.Xpath("")).SendKeys(text);<br>

