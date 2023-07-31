- It enables selecting an algorithm or strategy at runtime.
- It allows you to define a family of algorithms, encapsulate each one separately, and make them interchangeable.
- Clients can choose a specific algorithm from the available ones without knowing the details of the implementation.

**Components of the Strategy Design Pattern:**

1. **Context:** This is the class that holds a reference to the selected strategy object. It provides a method for clients to set or change the strategy.
    
2. **Strategy:** This is the interface or abstract class representing the algorithm's common contract. Concrete strategies implement this interface with specific algorithm variations.
    
3. **Concrete Strategy:** These are the classes that implement the `Strategy` interface, providing the actual algorithm's implementation.

using System;

// Strategy interface
interface ISortStrategy
{
    void Sort(int[] array);
}

// Concrete Strategies
class QuickSort : ISortStrategy
{
    public void Sort(int[] array)
    {
        Console.WriteLine("Sorting array using QuickSort.");
        // Implement QuickSort algorithm here
    }
}

class MergeSort : ISortStrategy
{
    public void Sort(int[] array)
    {
        Console.WriteLine("Sorting array using MergeSort.");
        // Implement MergeSort algorithm here
    }
}

// Context
class SortingContext
{
    private ISortStrategy sortStrategy;

    public void SetSortStrategy(ISortStrategy strategy)
    {
        this.sortStrategy = strategy;
    }

    public void Sort(int[] array)
    {
        sortStrategy.Sort(array);
    }
}

// Usage
class Program
{
    static void Main(string[] args)
    {
        SortingContext context = new SortingContext();

        int[] array = { 3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5 };

        // Use QuickSort strategy
        context.SetSortStrategy(new QuickSort());
        context.Sort(array);

        // Use MergeSort strategy
        context.SetSortStrategy(new MergeSort());
        context.Sort(array);
    }
}
