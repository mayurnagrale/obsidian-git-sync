- One-to-many dependency between objects
- When one object (the subject) changes its state, all its dependents (observers) are notified and updated automatically.
- This allows for loose coupling between the subject and its observers, enabling a flexible and maintainable design.

**Components of the Observer Design Pattern:**

1. Subject: This is the object that holds the state and manages the list of observers. It provides methods to attach, detach, and notify observers when its state changes.
    
2. Observer: This is the interface that defines the update method, which the concrete observers implement. The update method is called by the subject when there is a state change.
    
3. Concrete Subject: This is the actual subject class that maintains the state and sends notifications to its observers when the state changes.
    
4. Concrete Observer: This is the actual observer class that implements the update method to react to state changes in the subject.

using System;
using System.Collections.Generic;

// Observer interface
interface IObserver
{
    void Update(float temperature, float humidity, float pressure);
}

// Subject interface
interface ISubject
{
    void Attach(IObserver observer);
    void Detach(IObserver observer);
    void Notify();
}

// Concrete Subject (Weather Station)
class WeatherStation : ISubject
{
    private List<IObserver> observers = new List<IObserver>();
    private float temperature;
    private float humidity;
    private float pressure;

    public void Attach(IObserver observer)
    {
        observers.Add(observer);
    }

    public void Detach(IObserver observer)
    {
        observers.Remove(observer);
    }

    public void Notify()
    {
        foreach (var observer in observers)
        {
            observer.Update(temperature, humidity, pressure);
        }
    }

    public void SetMeasurements(float temperature, float humidity, float pressure)
    {
        this.temperature = temperature;
        this.humidity = humidity;
        this.pressure = pressure;
        Notify();
    }
}

// Concrete Observer (Display Device)
class DisplayDevice : IObserver
{
    public void Update(float temperature, float humidity, float pressure)
    {
        Console.WriteLine($"Display Device: Temperature={temperature}, Humidity={humidity}, Pressure={pressure}");
    }
}

// Usage
class Program
{
    static void Main(string[] args)
    {
        WeatherStation weatherStation = new WeatherStation();

        DisplayDevice displayDevice1 = new DisplayDevice();
        DisplayDevice displayDevice2 = new DisplayDevice();

        weatherStation.Attach(displayDevice1);
        weatherStation.Attach(displayDevice2);

        weatherStation.SetMeasurements(25, 60, 1013);
    }
}
