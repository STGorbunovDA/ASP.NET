# Важная Информация ASP.NET

**Инфа 1:**

*Глобальный cath*

- Вариант 1:

```
AppDomain.CurrentDomain.FirstChanceException
```

*Является событием, которое возникает, когда возникает первое исключение в приложении в определенном домене приложения (AppDomain).*

*Это событие позволяет обрабатывать исключения до того, как они будут переданы на уровень выше (например, глобальный обработчик исключений). Использование FirstChanceException может быть полезным для отладки и логирования исключений, а также для принятия нужных мер в случае их возникновения.*

*Например, вы можете зарегистрировать обработчик события FirstChanceException, чтобы сохранить информацию об исключении в журнале или отправить уведомление администратору. Это позволит вам более подробно изучить и понять причины возникновения исключений и быстрее реагировать на них.*

*Вот примеры кода, показывающие использование FirstChanceException :*

```C#
AppDomain.CurrentDomain.FirstChanceException += (sender, eventArgs) =>
{
    // Логирование или дополнительная обработка исключения
    Console.WriteLine($"Перехвачено первое исключение: {eventArgs.Exception}");
};

// Ваш код приложения
// ...
```

```C#
AppDomain.CurrentDomain.FirstChangeException += CurrentDomain_FirstChangeExeption;

public static void CurrentDomain_FirstChangeExeption(object? sender, System.Runtime.ExeptionService.FirstChanceExceptionEventArgs e)
{
    Сonsole.WriteLine(e.Exception);
}

```

*A так же ссылка на другую реализацию глобальной обработки исключений в ASP.NET Core приложении:*
 [habr.com](https://habr.com/ru/companies/otus/articles/543390/)


