# FINISHTASK
Репозиторий для итоговой контрольной работы по основному блоку
Решение задачи:
Создание метода string[] GetArrayStringConsole

создаем метод для разделения строки из консоли в массив по знаку “,”

string[] GetArrayStringConsole (string inConsolSimvol)
{
    string[] arraySimvol = new string[ConsolZnak];
    arraylZnak = ConsolZnak.Split(",");
    return arraylZnak;
}
Создание метода string[] GetArrayThreeZnak

создаем метод сортирующий символы из массива. сначала отсчитываем количество, удовлетворяющих требований, для определения длинны нового массива. создаем массив по выясненому количествуи заносим туда символы удовлетворяющие требованиям.

string[]GetArrayThreeZnak (string[] array)
{
    int count = 0;
    for (int i = 0; i < array.Length; i++)
    {
        string Znak = array[i];
        if (Znak.Length <= 3)
        {
            count++;
        }
    }
    string[] arrayThreeZnak = new string[count];
    for (int i = 0, j = 0; i < array.Length; i++)
    {
        string Znak = array[i];
        if (Znak.Length <= 3)
        {
            arrayThreeZnak[j] = simvol;
            j++;
        }
    }
    return arrayThreeZnak;
}
Создание метода void Print

создаем метод для вывода информации из массивов с использованием цеклического вывода каждого элемента массива.

void Print (string[] array)
{
    for (int i = 0; i < array.Length; i++)
    {
        Console.Write($"{array[i]}, ");
    }
    Console.WriteLine();
}
Создаем "клентский код" для вызова методов и обработки информации через консоль.
выводим поясняющую информационную строку для пользователя в консоле: "Введите массив через запятую (,) - ""Введите массив через запятую (,) - "

присваиваем введенное в консоле от пользователя символы string inStringZnak = console.ReadLine()
присваиваем массиву преобразованную строку через метод string[] arraylZnak = GetArrayStringConsole(inStringZnak)
Console.WriteLine(); Console.Write("Введенные символы - "); Print(GetArrayStringConsole(inStringZnak)); Console.WriteLine(); Console.Write("Массив из строк длинной меньше либо равны 3 - "); Print(GetArrayThreeZnak(arraylZnak)); Console.WriteLine();

Console.Write("Введите массив через запятую  (,) - ");
string inStringZnak = Console.ReadLine();
string[] arraySimvol = GetArrayStringConsole(inStringZnak);
Console.WriteLine();
Console.Write("Введенные символы - ");
Print(GetArrayStringConsole(inStringZnak));
Console.WriteLine();
Console.Write("Введенные символы длинной меньше либо равны 3 - ");
Print(GetArrayThreeZnak(arraylZnak));
Console.WriteLine();

