Console.WriteLine("Введите нижний предел значения матрицы");
int a = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите верхний предел значения матрицы");
int b = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите размер матрицы");
int n = Convert.ToInt32(Console.ReadLine());
int[,] ma = new int[n, n];
int[,] mb = new int[n, n];
int[,] mf = new int[n, n];
int[,] mv = new int[n, n];
Random random = new Random();
for (int i = 0; i < n; i++)
{
    for (int j = 0; j < n; j++)
    {
        ma[i, j] = random.Next(a, b);
    }
}
for (int i = 0; i < n; i++)
{
    for (int j = 0; j < n; j++)
    {
        mb[i, j] = random.Next(a, b);
    }
}
Console.WriteLine("Сложение");
for (int i = 0; i < n; i++)
{
    for (int j = 0; j < n; j++)
    {
        mf[i, j] = ma[i, j] + mb[i, j];
        Console.Write($"{mf[i, j]} \t");
    }
    Console.WriteLine();
}
Console.WriteLine();
Console.WriteLine("Вычетание");
for (int i = 0; i < n; i++)
{
    for (int j = 0; j < n; j++)
    {
        mv[i, j] = ma[i, j] - mb[i, j];
        Console.Write($"{mv[i, j]} \t");
    }
    Console.WriteLine();
}
