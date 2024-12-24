# Nader
Eng/Nader Mohammed 
// ==============================================
//    Program created by Eng. Nader Mohamed
// ==============================================
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲");
        Console.WriteLine("  Program created by Eng. Nader Mohamed");
        Console.WriteLine("▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲\n");

        // Input birth date
        Console.WriteLine("Enter your birth year: ");
        int birthYear = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter your birth month: ");
        int birthMonth = int.Parse(Console.ReadLine());

        Console.WriteLine("Enter your birth day: ");
        int birthDay = int.Parse(Console.ReadLine());

        // Get current date
        DateTime currentDate = DateTime.Now;

        // Calculate age
        int ageYear = currentDate.Year - birthYear;
        int ageMonth = currentDate.Month - birthMonth;
        int ageDay = currentDate.Day - birthDay;

        // Adjust for negative months
        if (ageMonth < 0)
        {
            ageYear--;
            ageMonth += 12;
        }

        // Adjust for negative days
        if (ageDay < 0)
        {
            ageMonth--;
            int previousMonth = (currentDate.Month == 1) ? 12 : currentDate.Month - 1;
            ageDay += DateTime.DaysInMonth(currentDate.Year, previousMonth);
        }

        // Display result
        Console.WriteLine($"\nYour age is: {ageYear} years, {ageMonth} months, and {ageDay} days.");
        Console.WriteLine("\n▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲");
        Console.WriteLine("         Thank you for using this program!");
        Console.WriteLine("▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲▲");
    }
}
