# Hijri Persian Calender Initializer
Every usage of DateTime becomes to Hijri simply by initializing the culture

# Culture_Hijri
Initilize persian culture means every usage of DateTime becomes to Hijri and there is no any concern and extra job needed.
Simply print datetime in Hijri by `DateTime.Now` or in SQL Server Transactions.
Persian Calender as default date/time culture.

Convert every use of DateTime to Persion Culture
Even SQL Server Transactions

Persian Hint:      تبدیل کلیه  تاریخ ها به هجری شمسی
  با یکبار فراخوانی اولیه این فایل

# How to Install

    Install-Package PersianCultureInitializer -Version 1.0.1   

# How to call the initilizer

## ASP.Net Core & ASP.Net 5+
Solution Explorer > Startup.cs
```csharp
         public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            ....
            Cultures.InitializePersianCulture(); // <----------------+ add these lines
            app.UseRequestLocalization();        // <----+
            ...

        }
```

## ASP.Net MVC Projects
Solution Explorer > Global.asax.cs
```csharp
        protected void Application_Start()
        {
            ...
            Cultures.InitializePersianCulture(); // <----------------- add this line
            ...

        }
```


## C# Console Projects

Solution Explorer > Program.cs
```csharp
     private static void Main()
        {
            ...
            Cultures.InitializePersianCulture(); // <------------------ add this line
            ...
        }
```


# Usage
Print the current date

```csharp
      var today = DateTime.Now;
      Console.WriteLine(today.ToLongDateString()); // 1400 شهریور 27, شنبه
      var year = today.Year;  // =1400
   // as you see there is no effort
```

Sql Server Queris
```csharp
  var today_books = _context.Books.Where(p=>p.RegisterDate.Date == DateTime.Now.Date);  // fetch books registered today
  foreach(var book in books)
        print(book.RegisterDate);  // 1400 شهریور 27, شنبه
```

## NuGet
[ PersianCultureInitializer ](https://www.nuget.org/packages/PersianCultureInitializer/1.0.1)
