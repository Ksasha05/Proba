# Справка по Selenium. (C#)
В основном как веб-драйвер использую Edge.

## Инициализация драйвера:
```
using OpenQA;
using OpenQA.Selenium;
using OpenQA.Selenium.Edge;

IWebDriver web = new EdgeDriver();
```

## Открыть ссылку:
```
web.Navigate().GoToUrl(link);
```

## Открыть ссылку в новом окне:
```
web.SwitchTo().NewWindow(WindowType.Tab);
web.Navigate().GoToUrl(link);
```

## Явное ожидание:
```
Thread.Sleep(7000);<br>
//В милисекундах
```

## Найти элемент на текущей странице:
```
web.FindElement(By.Xpath(""));
//Я использую Xpath(удобно через расширение в браузере смотреть), в кавычках пишется путь к элементу странице<br>
в виде XML - //p[@class='wa-overview__title']
```

## Нажатие на элемент:
```
web.FindElement(By.Xpath("")).Click();
```

## Выбрать текст элемента:
```
string text = web.FindElement(By.Xpath("")).Text;
```

## Вставить значение в элемент(например в поле ввода):
```
string text = "text";
web.FindElement(By.Xpath("")).SendKeys(text);
```

## Собрать весь html-код страницы:
```
                web.Navigate().GoToUrl(url);
                text = web.PageSource;
```
