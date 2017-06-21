using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Car_To_Go
{
    class Program
    {
        static void Main(string[] args)
        {
            decimal budget = decimal.Parse(Console.ReadLine());
            string season = Console.ReadLine().ToLower();
            string cl = String.Empty;
            string car = String.Empty;

            if (budget <= 100)
            {
                cl = "Economy class";

                switch (season)
                {
                    case "summer": budget *= 0.35m; car = "Cabrio"; break;
                    case "winter": budget *= 0.65m; car = "Jeep"; break;
                }
            }
            else if (budget <= 500)
            {
                cl = "Compact class";

                switch (season)
                {
                    case "summer": budget *= 0.45m; car = "Cabrio"; break;
                    case "winter": budget *= 0.80m; car = "Jeep"; break;
                }
            }
            else
            {
                cl = "Luxury class";

                budget *= 0.90m;
                car = "Jeep";
            }
            Console.WriteLine(cl);
            Console.WriteLine($"{car} - {budget:f2}");
        }
    }
}

