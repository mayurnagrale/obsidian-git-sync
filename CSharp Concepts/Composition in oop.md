public class Car
{
    private Engine engine;
    private Wheel[] wheels;

    public Car()
    {
        engine = new Engine();
        wheels = new Wheel[4];
        for (int i = 0; i < 4; i++)
        {
            wheels[i] = new Wheel();
        }
    }
}


In this example, the `Car` class is composed of an `Engine` and an array of `Wheel` objects. When a `Car` object is created, its parts (engine and wheels) are also created. When the `Car` object is destroyed, its parts are also destroyed.