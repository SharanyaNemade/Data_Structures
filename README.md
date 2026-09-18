# Data_Structures






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

     for(int i = 0; i < numbers.length; i++)
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
