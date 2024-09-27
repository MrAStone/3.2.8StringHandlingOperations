```c#
using System;
using System.Collections.Generic;
using System.Data.SqlTypes;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace _3._2._8StringHandlingOperations
{
    internal class Program
    {
        static void Main(string[] args)
        {
            // Understand and be able to use:
            string myStringToUse = "This is a string";
            // length
            Console.WriteLine(myStringToUse.Length);
            // position
            Console.WriteLine(myStringToUse[0]); // the first character in a string (T)
            Console.WriteLine(myStringToUse[myStringToUse.Length - 1]); // the last character in a string (g)
            // substring
            Console.WriteLine(myStringToUse.Substring(2, 7)); //start at index 2 and output length of 7 (is is a)
            Console.WriteLine(myStringToUse.Substring(5)); // start at index 5 and go to the end of the string (is a string)

            // concatenation
            Console.WriteLine("my string is " +  myStringToUse); // concatenation with +
            Console.WriteLine($"my string is {myStringToUse}"); // string builder uses $ before string and {variable name} in the string itself
            Console.WriteLine("my string is {0}", myStringToUse); // string builder uses parameter {param number} and comma separated parameters
            string first = "Something";
            string second = "other Thing";
            Console.WriteLine(myStringToUse +  first + second);
            Console.WriteLine($"{myStringToUse} {first} {second}");
            Console.WriteLine("joining with parameters, {0} {1} {2}",myStringToUse,first,second);


            // convert character to character code
            char myChar = 'A';
            Console.WriteLine(Convert.ToInt32(myChar));
            myChar = 'a';
            Console.WriteLine(Convert.ToInt32(myChar));
            // convert character code to character
            int charCode = 65;
            Console.WriteLine(Convert.ToChar(charCode));
            for (int i = 65; i < 91; i++)
            {
                Console.WriteLine(Convert.ToChar(i));
            }
            // string conversion operations.
            //  Expected string conversion operations:
            // string to integer
            int numberInput;
            string stringInput;
            // take a string input and convert
            Console.WriteLine("Enter a number: ");
            stringInput = Console.ReadLine();
            numberInput = Convert.ToInt32(stringInput);

            // Convert as entering value
            Console.WriteLine("Enter a number: ");
            numberInput = Convert.ToInt32(Console.ReadLine());

            // string to real

            double doubleInput;
            Console.WriteLine("Enter a real number: ");
            stringInput = Console.ReadLine() ;
            doubleInput = Convert.ToDouble(stringInput);

            Console.WriteLine("Enter a real number: ");
            doubleInput = Convert.ToDouble(Console.ReadLine());

            // integer to string
            string stringOutput;
            stringOutput = Convert.ToString(numberInput);
            stringOutput = numberInput.ToString();

            // real to string
            stringOutput = Convert.ToString(doubleInput);
            stringOutput = doubleInput.ToString();

        }
    }
}
```
