public class Converter
{
    public double ConvertToDouble(int value)
    {
        return (double)value;
    }

    public double ConvertToDouble(string value)
    {
        double result;
        double.TryParse(value, out result);
        return result;
    }
}
