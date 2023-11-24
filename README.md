using System;
using System.Collections.Generic;

// Define the Farm class
class Farm
{
    // Properties
    public string Name { get; set; }
    public int ID { get; set; }
    public string Number { get; set; }
    public string Type { get; set; }
    public DateTime Date { get; set; }
    //public List<Animal> Animals { get; set; }

    // Constructor
    public Farm(string name)
    {
        Name = name;
        Animals = new List<Animal>();
    }

    // Method to add an animal to the farm
    public void AddAnimal(Animal animal)
    {
        Animals.Add(animal);
    }

    // Method to display the farm details
    public void DisplayFarm()
    {
        Console.WriteLine($"Farm Name: {Name}");
        Console.WriteLine("Animals:");
        foreach (Animal animal in Animals)
        {
            Console.WriteLine($"- {animal.Name} ({animal.Type})");
        }
    }
}

// Define the Animal class
class Animal 
{
    // Properties
    public string Name { get; set; }
    public int ID { get; set; }
    public string Number { get; set; }
    public string Type { get; set; }
    public DateTime Date { get; set; }

    // Constructor
    public Animal(string name, string type, string id, string date, int number)
    {
        Name = name;
        Type = type;
        ID = id;
        Date = date;
        Number = number;

    }
}

// Main program
class Program
{
    static void Main(string[] args)
    {
        // Create a farm
        //Farm myFarm = new Farm("My Farm");

        // Add animals to the farm
        // Animal cow = new Animal("Bessie", "Cow", "1", "1234", 2003);
        // myFarm.AddAnimal(cow);

        // Animal pig = new Animal("Porky", "Pig", "2", "3456", 2004 );
        // myFarm.AddAnimal(pig);

        // // Display the farm details
        // myFarm.DisplayFarm();

        // Create a farm object
        Farm farm = new Farm();
        farm.Name = "My Farm";
        farm.ID = 1;
        farm.Number = "123";
        farm.Type = "Dairy";
        farm.Date = DateTime.Now;

        // Create an animal object
        Animal animal = new Animal();
        animal.Name = "Cow";
        animal.ID = 1;
        animal.Number = "456";
        animal.Type = "Holstein";
        animal.Date = DateTime.Now;

        // Display farm and animal information
        Console.WriteLine("Farm Information:");
        Console.WriteLine("Name: " + farm.Name);
        Console.WriteLine("ID: " + farm.ID);
        Console.WriteLine("Number: " + farm.Number);
        Console.WriteLine("Type: " + farm.Type);
        Console.WriteLine("Date: " + farm.Date);

        Console.WriteLine();

        Console.WriteLine("Animal Information:");
        Console.WriteLine("Name: " + animal.Name);
        Console.WriteLine("ID: " + animal.ID);
        Console.WriteLine("Number: " + animal.Number);
        Console.WriteLine("Type: " + animal.Type);
        Console.WriteLine("Date: " + animal.Date);

        Console.ReadLine();
    }
}
