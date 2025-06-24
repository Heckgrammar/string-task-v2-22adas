namespace ExtractingStringPartsTask
{
    internal class Program
    {
        static void Main(string[] args)
        {
            string country = "United States of America";
            string state = "California";
            string city = "San Fransicso";
            string landmark = "Alcatraz Island";

            Console.WriteLine(state.Length);
            Console.WriteLine(city + " " + landmark);
            Console.WriteLine(country[0]);
            Console.WriteLine(city[0] + "" + city[city.Length - 1]);

            int cIndex = landmark.ToLower().IndexOf('c');
            if (cIndex != -1)
                Console.WriteLine(landmark.Substring(cIndex));
            else
                Console.WriteLine("Character 'c' not found");

            int sIndex = country.IndexOf('S');
            int aIndex = country.IndexOf('A', sIndex);
            if (sIndex != -1 && aIndex != -1 && aIndex > sIndex)
                Console.WriteLine(country.Substring(sIndex, aIndex - sIndex + 1));
            else
                Console.WriteLine("No valid substring from 'S' to 'A' found");

            Console.WriteLine(state.IndexOf('f'));
        }
    }
}
