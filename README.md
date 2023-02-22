//Напишите программу, которая на вход принимает позиции элемента в двумерном массиве, и возвращает значение этого элемента или же указание, что такого элемента нет.

//Например, задан массив:

//1 4 7 2

//5 9 2 3

//8 4 2 4

//17 -> такого числа в массиве нет

void Znach(double[,] a, int m, int n)

{

  bool flag = false;  
  
  Console.WriteLine("Введите позицию искомого элемента: ");
  
  int k = Convert.ToInt32(Console.ReadLine());
  
  int l = Convert.ToInt32(Console.ReadLine());
  
  for (int i = 0; i < m;i++)
  
{

    for (int j =0; j<n; j++)
    
    {
    
        if (k == i && l == j)
        
        {
        
           flag = true;
           
           Console.WriteLine(a[i,j]); 
           
        }
        
    }
    
}

if (flag == false)

{
    Console.WriteLine("Элемента на такой позиции нет");
} 

}

Console.WriteLine("Введите количество строк: ");

int m = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Введите количество столбцов: ");

int n = Convert.ToInt32(Console.ReadLine());

double[,] a = new double[m,n];

for (int i = 0; i < m;i++)

{

    for (int j =0; j<n; j++)
    
    {
    
        a[i,j] = new Random().Next(-10,11);
        
        Console.Write(string.Format("{0} ", a[i, j]));
        
    }
    
    Console.Write(Environment.NewLine + Environment.NewLine);
    
}

Znach(a,m,n);
