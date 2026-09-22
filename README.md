# Data_Structures

**Array Traversal**

**1. Print all elements of an array**



using System;
class HelloWorld 
{
  static void Main()
   {
    int[] numbers = { 10, 20, 30, 40, 50 };
    for (int i = 0; i < numbers.Length; i++)
    {
      Console.WriteLine(numbers[i]);
    }
  }
}





**2. Find the sum of all elements**




using System;
class HelloWorld
{
   static void Main()
   {
     int[] numbers = {1,2,3,4,5,6,7,8,9};
     int sum = 0;

     for(int i = 0; i < numbers.Length; i++)
     {
        sum = sum + numbers[i];
     }
     Console.WriteLine(sum);
   }
}





**3. Find the largest element**



using System;
class HelloWorld
{
   static void Main()
   {
      int[] numbers = { 10, 5, 30, 20 };
      int largest = numbers[0];
      
      for (int i = 1; i < numbers.Length; i++)
     {
       if (numbers[i] > largest)
      {
        largest = numbers[i];
      }
     }

Console.WriteLine(largest);
   }
}





**4. Find the smallest element**




using System;
class HelloWorld
{
  static void Main()
  {
    int[] numbers = {10,5,30,20};
    int smallest = numbers[0];

    for(int i = 1; i < numbers.Length; i++)
    { 
    	if(numbers[i] < smallest)
	{
	   smallest = numbers[i];
	}
    }
	Console.WriteLine(smallest);
  }
}





**5. Count even and odd numbers**




using System;
class HelloWorld
{
  static void Main()
  {
    
    int[] numbers = {0,1,2,3,4,5,6,7,8,9,10};
    
    int evenCount = 0;
    int oddCount = 0;
    
    for(int i = 0; i < numbers.Length; i++)
    {
        if(numbers[i] % 2 == 0)
        {
            evenCount++;
        }
        
        else
        {
            oddCount++;
        }
    }
    
    Console.WriteLine("Even = " + evenCount);
    Console.WriteLine("Even = " + oddCount);
    
  }
}





**6. Calculate average of array elements**




using System;
class HelloWorld
{
  static void Main()
  {
    
    int[] numbers = { 10, 20, 30, 40 };

    int sum = 0;

    for (int i = 0; i < numbers.Length; i++)
    {
        sum += numbers[i];
    }

    double average = (double)sum / numbers.Length;

    Console.WriteLine(average);
    
  }
}






**7. Find Second Largest**





using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 50, 20, 40, 30 };

        int largest = numbers[0];
        int secondLargest = numbers[0];

        for (int i = 1; i < numbers.Length; i++)
        {
            if (numbers[i] > largest)
            {
                secondLargest = largest;
                largest = numbers[i];
            }
            else if (numbers[i] > secondLargest && numbers[i] != largest)
            {
                secondLargest = numbers[i];
            }
        }

        Console.WriteLine("Largest = " + largest);
        Console.WriteLine("Second Largest = " + secondLargest);
    }
}





**8. Find Second Smallest**





using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 50, 20, 40, 30 };

        int smallest = numbers[0];
        int secondSmallest = numbers[0];

        for (int i = 1; i < numbers.Length; i++)
        {
            if (numbers[i] < smallest)
            {
                secondSmallest = smallest;
                smallest = numbers[i];
            }
            else if (numbers[i] < secondSmallest && numbers[i] != smallest)
            {
                secondSmallest = numbers[i];
            }
        }

        Console.WriteLine("Smallest = " + smallest);
        Console.WriteLine("Second Smallest = " + secondSmallest);
    }
}






**9. Reverse an array**



using System;
class HelloWorld
{
  static void Main()
  {
    int[] numbers = { 1, 2, 3, 4, 5 };

	int left = 0;
	int right = numbers.Length - 1;

while (left < right)
{
    int temp = numbers[left];

    numbers[left] = numbers[right];
    numbers[right] = temp;

    left++;
    right--;
}

Console.WriteLine(string.Join(", ", numbers));
  }
}




**10. Move all zeroes to the end**



using System;
class HelloWorld
{
  static void Main()
  {
    int[] numbers = { 0, 1, 0, 3, 12 };

    int index = 0;

    for (int i = 0; i < numbers.Length; i++)
    {
        if (numbers[i] != 0)
    {
        numbers[index] = numbers[i];
        index++;
    }
}

while (index < numbers.Length)
{
    numbers[index] = 0;
    index++;
}

Console.WriteLine(string.Join(", ", numbers));
  }
}




**11. Move negative numbers to one side**



using System;
class HelloWorld
{
  static void Main()
  {
    int[] numbers = { -1, 2, -3, 4, -5, 6 };

    int left = 0;
    int right = numbers.Length - 1;


    while (left <= right)
    {
        if (numbers[left] < 0)
    {
        left++;
    }
    
    else if (numbers[right] >= 0)
    {
        right--;
    }
    
    else
    {
        int temp = numbers[left];
        numbers[left] = numbers[right];
        numbers[right] = temp;

        left++;
        right--;
    }
}

Console.WriteLine(string.Join(", ", numbers));
  }
}






**12. Difference between maximum and minimum**




using System;
class HelloWorld
{
  static void Main()
  {
    int[] numbers = { 10, 5, 30, 20 };

    int max = numbers[0];
    int min = numbers[0];

    for (int i = 1; i < numbers.Length; i++)
    {
        if (numbers[i] > max)
        {
            max = numbers[i];
        }

    if (numbers[i] < min)
        {
            min = numbers[i];
        }
    }

    int difference = max - min;

    Console.WriteLine("Maximum = " + max);
    Console.WriteLine("Minimum = " + min);
    Console.WriteLine("Difference = " + difference);
  }
}




**Array Insertion / Deletion**



**1. Insert an element at the beginning**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int insertValue = 5;

        int[] newArray = new int[numbers.Length + 1];

        newArray[0] = insertValue;

        for (int i = 0; i < numbers.Length; i++)
        {
            newArray[i + 1] = numbers[i];
        }

        Console.WriteLine("Array after insertion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**2. Insert an element at the end**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int insertValue = 50;

        int[] newArray = new int[numbers.Length + 1];

        for (int i = 0; i < numbers.Length; i++)
        {
            newArray[i] = numbers[i];
        }

        newArray[numbers.Length] = insertValue;

        Console.WriteLine("Array after insertion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**3. Insert an element at a specific index**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int insertValue = 25;
        int index = 2;

        int[] newArray = new int[numbers.Length + 1];

        for (int i = 0; i < index; i++)
        {
            newArray[i] = numbers[i];
        }

        newArray[index] = insertValue;

        for (int i = index; i < numbers.Length; i++)
        {
            newArray[i + 1] = numbers[i];
        }

        Console.WriteLine("Array after insertion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}





**4. Delete the first element**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int[] newArray = new int[numbers.Length - 1];

        for (int i = 1; i < numbers.Length; i++)
        {
            newArray[i - 1] = numbers[i];
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}




**5. Delete the last element**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int[] newArray = new int[numbers.Length - 1];

        for (int i = 0; i < numbers.Length - 1; i++)
        {
            newArray[i] = numbers[i];
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}




**6. Delete an element from a specific index**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40 };

        int deleteIndex = 2;

        int[] newArray = new int[numbers.Length - 1];

        for (int i = 0; i < deleteIndex; i++)
        {
            newArray[i] = numbers[i];
        }

        for (int i = deleteIndex; i < numbers.Length - 1; i++)
        {
            newArray[i] = numbers[i + 1];
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**7. Insert Multiple Elements at a Given Position**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40, 50 };

        int[] insertValues = { 100, 200 };

        int index = 2;

        int newLength = numbers.Length + insertValues.Length;

        int[] newArray = new int[newLength];

        // Copy elements before insertion index
        for (int i = 0; i < index; i++)
        {
            newArray[i] = numbers[i];
        }

        // Insert new elements
        for (int i = 0; i < insertValues.Length; i++)
        {
            newArray[index + i] = insertValues[i];
        }

        // Copy remaining elements
        for (int i = index; i < numbers.Length; i++)
        {
            newArray[i + insertValues.Length] = numbers[i];
        }

        Console.WriteLine("Array after insertion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**8. Delete All Occurrences of a Given Value**


using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 10, 30, 10, 40 };

        int deleteValue = 10;

        // Count elements that should remain
        int count = 0;

        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] != deleteValue)
            {
                count++;
            }
        }

        int[] newArray = new int[count];

        int index = 0;

        // Copy elements except deleteValue
        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] != deleteValue)
            {
                newArray[index] = numbers[i];
                index++;
            }
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**9. Remove an Element Without Using LINQ**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40, 50 };

        int deleteValue = 30;

        int deleteIndex = -1;

        // Find the index of the value
        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] == deleteValue)
            {
                deleteIndex = i;
                break;
            }
        }

        // Check whether value was found
        if (deleteIndex == -1)
        {
            Console.WriteLine("Element not found.");
            return;
        }

        int[] newArray = new int[numbers.Length - 1];

        // Copy elements before deleted index
        for (int i = 0; i < deleteIndex; i++)
        {
            newArray[i] = numbers[i];
        }

        // Shift remaining elements
        for (int i = deleteIndex; i < newArray.Length; i++)
        {
            newArray[i] = numbers[i + 1];
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}



**10. Remove an Element While Maintaining the Original Order**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40, 50 };

        int deleteValue = 30;

        int[] newArray = new int[numbers.Length - 1];

        int index = 0;

        bool found = false;

        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] == deleteValue && !found)
            {
                found = true;
                continue;
            }

            newArray[index] = numbers[i];
            index++;
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}




**11. Remove an Element Without Maintaining Order**



using System;

class HelloWorld
{
    static void Main()
    {
        int[] numbers = { 10, 20, 30, 40, 50 };

        int deleteValue = 20;

        int deleteIndex = -1;

        // Find the element
        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] == deleteValue)
            {
                deleteIndex = i;
                break;
            }
        }

        if (deleteIndex == -1)
        {
            Console.WriteLine("Element not found.");
            return;
        }

        int[] newArray = new int[numbers.Length - 1];

        // Copy all elements except deleted element
        for (int i = 0; i < numbers.Length - 1; i++)
        {
            if (i == deleteIndex)
            {
                newArray[i] = numbers[numbers.Length - 1];
            }
            else
            {
                newArray[i] = numbers[i];
            }
        }

        Console.WriteLine("Array after deletion:");

        for (int i = 0; i < newArray.Length; i++)
        {
            Console.Write(newArray[i] + " ");
        }
    }
}


