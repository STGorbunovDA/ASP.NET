# Ошибки ASP.NET

**Ошибка 1:**

*При начальном создании проекта Net Core 6.0 ASP Net MVC появляется данная ошибка*

![picture for error_1](https://github.com/STGorbunovDA/ASP.NET/blob/main/source/img/error_1.png)

**Решение:**

*Добавить Program.cs :*

```
builder.Services.AddRazorPages().AddRazorRuntimeCompilation();
```
*И добавить следующую ссылку на пакет в файл проекта :*
```
<ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation" Version="6.0.3" />
</ItemGroup>
```
*Отметим, что для производственного окружения компиляции 
в реальном времени обычно не рекомендуется из-за возможных проблем с производительностью и безопасностью.*

**Ошибка 2:**

*Консоль диспетчера пакетов отображает неверную кодировку*

![picture for error_1](https://github.com/STGorbunovDA/ASP.NET/blob/main/source/img/error_2.png)

**Решение:**

*В терминале консоли ввести :*

```
setx DOTNET_CLI_UI_LANGUAGE "en-US"
```
*Перезагрузить VS*
