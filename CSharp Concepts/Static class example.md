public static class Sample
    {
        public const string Name="M";
        public static readonly string xName;
        public static string LName = "N";
        public static int Add(int a,int b,string x)
        {
            LName = x;
            return a + b;
        }

        public static void Substract(int a,int b)
        {
            int c = a - b;
            Console.WriteLine(c);
        }
    }