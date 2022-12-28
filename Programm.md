
# Основной код программы представлен ниже

1. Первая часть вывод необработтанного и обработанного массива.

```
Console.Clear();
string[] array = { "hello", "2", "world", ":-)" };
string[] array1 = { "1234", "1567", "-2", "computer science" };
string[] array2 = { "Russia", "Denmark", "Kazan" };

Console.WriteLine();
Console.WriteLine(String.Join(",", array));
string[] newarray = ShowNewArray(array);
Console.Write($"[{string.Join(",", newarray).Trim(',')}]");

Console.WriteLine();
Console.WriteLine(String.Join(",", array1));
string[] newarray1 =(ShowNewArray(array1));
Console.Write($"[{string.Join(",", newarray1).Trim(',')}]");

Console.WriteLine();
Console.WriteLine(String.Join(",", array2));
string[] newarray2 = ShowNewArray(array2);
Console.Write($"[{string.Join(",", newarray2).Trim(',')}]");
```
---
2. Вторая часть метод обработки массива String.
```

string[] ShowNewArray(string[] inputarray)
{
    int temp = 3; 

    string[] outputarray = new string[1]; 

    for (int i = 0; i < inputarray.Length; i++) 
    

        for (int j = 0; j < outputarray.Length; j++) 
        {
            if (inputarray[i].Length <= temp) 
                outputarray[j] += inputarray[i] + ",";
        }
    
    return outputarray;
}

}
```