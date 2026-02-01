using System;

public class Logger
{
    public void Log(string level, string message)
    {
        Console.WriteLine($"{level}: {message}");
    }
}

public static class AppConfig
{
    public static string ConnectionString =
        "Server=myServer;Database=myDb;User Id=myUser;Password=myPass;";
}

public class DatabaseService
{
    public void Connect()
    {
        string connectionString = AppConfig.ConnectionString;
    }
}

public class LoggingService
{
    public void Log(string message)
    {
        string connectionString = AppConfig.ConnectionString;
    }
}
