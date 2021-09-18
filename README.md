# Hijri Persian Calender Initializer
Every usage of DateTime becomes to Hijri simply by initializing the culture

# Culture_Hijri
Initilize persian culture means every usage of DateTime becomes to Hijri and there is no any concern and extra job needed.
Simply print datetime in Hijri by `DateTime.Now` or in SQL Server Transactions.
Persian Calender as default date/time culture.

Convert every use of DateTime to Persion Culture
Even SQL Server Transactions

![Screenshot](Peyman.HijriPersianCalenderInitializer/Banner.png)

Persian Hint:      تبدیل کلیه  تاریخ ها به هجری شمسی
  با یکبار فراخوانی اولیه این فایل
   
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


