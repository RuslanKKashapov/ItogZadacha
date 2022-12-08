# ItogZadacha
Итоговая проверочная работа Кашапов Р.К. Курс Разработчик

1. Создаать репозиторий на GitHub
2. Нарисовать блок-схему алгоритма
3. Снабдить репозиторий оформленным текстом описания решения
4. Написать программу, решающую поставленную задачу
5. Использовать контроль версий в работе

Решение
2.

![image](https://user-images.githubusercontent.com/114429115/206553577-6c52a305-1e69-4f3b-b259-ea0030d0566e.png)

Решение 
4.

Console.Clear();

string[] array = GetArray();
string[] result = Find(array, 3);
Console.WriteLine($"[{string.Join(", ", array)}] -> [{string.Join(", ", result)}]");

string[] Find(string[] input, int n)
{
    string[] output = new string[Count(input, n)];

    for (int i = 0, j = 0; i < input.Length; i++)
    {
        if (input[i].Length <= n)
        {
            output[j] = input[i];
            j++;
        }
    }

    return output;
}

int Count(string[] input, int n)
{
    int count = 0;

    for (int i = 0; i < input.Length; i++)
    {
        if (input[i].Length <= n)
        {
            count++;
        }
    }
    return count;
}

string[] GetArray()
{
    Console.Write("Введите элементы массива через пробел: ");
    return 
    Console.ReadLine().Split(" ");
}
