# Rectangle46


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SENG8040_Assignment1
{
    class Program
    {
        public static int SelectAnyfromMenu()
        {
            string custInput = "";
            bool validSelection = false;

            while (validSelection == false)
            {
                Console.WriteLine("1. Get Rectangle Length");
                Console.WriteLine("2. Change Rectangle Length");
                Console.WriteLine("3. Get Rectangle Width");
                Console.WriteLine("4. Change Rectangle Width");
                Console.WriteLine("5. Get Rectangle Perimeter");
                Console.WriteLine("6. Get Rectangle Area");
                Console.WriteLine("7. Exit");

                Console.WriteLine("\nHey Hi! Please select any one from the above Menu: \n");
                custInput = Console.ReadLine();

                if (custInput != "1" && custInput != "2" && custInput != "3" && custInput != "4" &&
                    custInput != "5" && custInput != "6" && custInput != "7")
                {
                    Console.WriteLine("Invalid Option, Select from 1 to 7\n");
                }
                else
                {
                    validSelection = true;
                }
            }
            Console.WriteLine();
            return int.Parse(custInput);
        }

        public static int ValidateCustInput(string selectedNumber)
        {
            int singleNumber = 1;
            bool isValid = false;
            while (isValid == false)
                try
                {
                    {
                        Console.WriteLine($"Please enter the {selectedNumber}:");
                        string custInput = Console.ReadLine();
                        int conCustInput = Int32.Parse(custInput);

                        if (conCustInput < 0)
                        {
                            Console.WriteLine("Negative not allowed\n");
                        }
                        else
                        {
                            bool result = int.TryParse(custInput, out singleNumber);
                            if (result == false)
                            {
                                Console.WriteLine("Invalid input, Try again.\n");
                            }
                            else
                            {
                                isValid = true;
                                Console.WriteLine($"Your {selectedNumber} has been altered to: {singleNumber}.\n");
                            }
                        }
                    }
                }
                catch (Exception)
                {
                    Console.WriteLine("Characters & Special Characters are not allowed!!!\n");
                }
            return singleNumber;
        }

        static void Main(string[] args)
        {
            Rectangle46 rect = new Rectangle46();
            int pick;
            int lengthInt;
            int widthInt;
            lengthInt = ValidateCustInput("Length");
            widthInt = ValidateCustInput("Width");
            Console.WriteLine($"Your Length & Width are {lengthInt} and {widthInt}.\n");
            Rectangle46 customRect = new Rectangle46(lengthInt, widthInt);
            rect = customRect;
            pick = SelectAnyfromMenu();

            while (pick != 7)
            {
                int result;
                switch (pick)
                {
                    case 1:
                        Console.WriteLine($"Length is: {rect.GetLength()}\n");
                        break;
                    case 2:
                        result = ValidateCustInput("Length");
                        rect.SetLength(result);
                        break;
                    case 3:
                        Console.WriteLine($"Width is: {rect.GetWidth()}\n");
                        break;
                    case 4:
                        result = ValidateCustInput("Width");
                        rect.SetWidth(result);
                        break;
                    case 5:
                        Console.WriteLine($"The result of (2*{rect.GetLength()} + {rect.GetWidth()}) is: {rect.GetPerimeter()}\n");
                        break;
                    case 6:
                        Console.WriteLine($"The result of {rect.GetLength()} * {rect.GetWidth()} is: {rect.GetArea()}\n");
                        break;
                    default:
                        break;
                }
                pick = SelectAnyfromMenu();
            }
        }
    }
}
