using System;

public class OrderService
{
    private void PrintOrder(string action, string productName, int quantity, double price)
    {
        double totalPrice = quantity * price;
        Console.WriteLine($"Order for {productName} {action}. Total: {totalPrice}");
    }

    public void CreateOrder(string productName, int quantity, double price)
    {
        PrintOrder("created", productName, quantity, price);
    }

    public void UpdateOrder(string productName, int quantity, double price)
    {
        PrintOrder("updated", productName, quantity, price);
    }
}

public abstract class Vehicle
{
    public void Start()
    {
        Console.WriteLine($"{this.GetType().Name} is starting");
    }

    public void Stop()
    {
        Console.WriteLine($"{this.GetType().Name} is stopping");
    }
}

public class Car : Vehicle { }
public class Truck : Vehicle { }

public class SimpleCalculator
{
    public int Add(int a, int b)
    {
        return a + b;
    }
}

public class SimpleAction
{
    public void DoSomething()
    {
        Console.WriteLine("Doing something simple...");
    }
}

public class Circle
{
    private double _radius;

    public Circle(double radius)
    {
        _radius = radius;
    }

    public double CalculateArea()
    {
        return Math.PI * _radius * _radius;
    }
}

public class MathOperations
{
    public int Add(int a, int b)
    {
        return a + b;
    }
}

class Program
{
    static void Main()
    {
        while (true)
        {
            Console.WriteLine("\nВыберите принцип для демонстрации:");
            Console.WriteLine("1 - DRY");
            Console.WriteLine("2 - KISS");
            Console.WriteLine("3 - YAGNI");
            Console.WriteLine("0 - Выход");
            Console.Write("Ваш выбор: ");

            string choice = Console.ReadLine();

            switch (choice)
            {
                case "1":
                    RunDry();
                    break;
                case "2":
                    RunKiss();
                    break;
                case "3":
                    RunYagni();
                    break;
                case "0":
                    return;
                default:
                    Console.WriteLine("Неверный выбор. Попробуйте снова.");
                    break;
            }
        }
    }

    static void RunDry()
    {
        Console.Write("Введите название товара: ");
        string product = Console.ReadLine();

        Console.Write("Введите количество: ");
        int qty = int.Parse(Console.ReadLine());

        Console.Write("Введите цену: ");
        double price = double.Parse(Console.ReadLine());

        OrderService service = new OrderService();
        service.CreateOrder(product, qty, price);
        service.UpdateOrder(product, qty + 1, price);

        Vehicle car = new Car();
        car.Start();
        car.Stop();

        Vehicle truck = new Truck();
        truck.Start();
        truck.Stop();
    }

    static void RunKiss()
    {
        SimpleCalculator calc = new SimpleCalculator();

        Console.Write("Введите число a: ");
        int a = int.Parse(Console.ReadLine());
        Console.Write("Введите число b: ");
        int b = int.Parse(Console.ReadLine());

        Console.WriteLine($"Сумма: {calc.Add(a, b)}");

        SimpleAction action = new SimpleAction();
        action.DoSomething();
    }

    static void RunYagni()
    {
        Console.Write("Введите радиус круга: ");
        double r = double.Parse(Console.ReadLine());

        Circle circle = new Circle(r);
        Console.WriteLine($"Площадь круга: {circle.CalculateArea()}");

        MathOperations math = new MathOperations();
        Console.Write("Введите число a: ");
        int a = int.Parse(Console.ReadLine());
        Console.Write("Введите число b: ");
        int b = int.Parse(Console.ReadLine());

        Console.WriteLine($"Сумма: {math.Add(a, b)}");
    }
}
