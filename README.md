using System;

public class Shape
{
    private string color;
    private bool filled;
    public Shape()
    {
        color = "green";
        filled = true;
    }
    public Shape(string color, bool filled)
    {
        this.color = color;
        this.filled = filled;
    }
    public string GetColor()
    {
        return color;
    }

    public void SetColor(string color)
    {
        this.color = color;
    }
    public bool IsFilled()
    {
        return filled;
    }

    public void SetFilled(bool filled)
    {
        this.filled = filled;
    }
    public override string ToString()
    {
        string filledStatus = filled ? "filled" : "not filled";
        return $"A Shape with color of {color} and {filledStatus}.";
    }
}
public class Program
{
    public static void Main(string[] args)
    {
        Shape shape1 = new Shape();
        Console.WriteLine("Default Shape:");
        Console.WriteLine(shape1.ToString()); 
        Shape shape2 = new Shape("blue", false);
        Console.WriteLine("\nCustom Shape:");
        Console.WriteLine(shape2.ToString());
        shape2.SetColor("red");
        shape2.SetFilled(true);
        Console.WriteLine("\nModified Shape:");
        Console.WriteLine(shape2.ToString());
    }
}
