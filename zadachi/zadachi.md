// Задача 54: Задайте двумерный массив. Напишите программу, 
// которая упорядочит по убыванию элементы каждой строки двумерного массива.
// Например, задан массив:
// 1 4 7 2
// 5 9 2 3
// 8 4 2 4
// В итоге получается вот такой массив:
// 7 4 2 1
// 9 5 3 2
// 8 4 4 2


// int rows = ReadInt("Введите количество строк: ");
// int colums = ReadInt("Введите количество столбцов: ");
// int[,] numbers = new int[rows, colums];
// FillRandomArray2D(numbers);
// PrintArray2D(numbers);
// SortToLowerArray2D(numbers);
// Console.WriteLine();
// PrintArray2D(numbers);

// // Функция заполнения массива рандомными числами от 1 до 9
// void FillRandomArray2D(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             array[i, j] = new Random().Next(1, 10);
//         }
//     }
// }

// // Функция вывода двумерного массива
// void PrintArray2D(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             Console.Write(array[i, j] + " ");
//         }
//         Console.WriteLine();
//      }
// }

// // Функция сортировки элементов в строке двумерного массива, по убыванию
// void SortToLowerArray2D(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             for (int k = 0; k < array.GetLength(1) - 1; k++)
//             {
//                 if (array[i, k] < array[i, k + 1])
//                 {
//                     int temp = array[i, k + 1];
//                     array[i, k + 1] = array[i, k];
//                     array[i, k] = temp;
//                 }
//             }
//         }
//     }
// }

// int ReadInt(string message)
// {
//     Console.Write(message);
//     return Convert.ToInt32(Console.ReadLine());
// }



// Задача 56: Задайте прямоугольный двумерный массив. Напишите программу, 
// которая будет находить строку с наименьшей суммой элементов.
// Например, задан массив:
// 1 4 7 2
// 5 9 2 3
// 8 4 2 4
// 5 2 6 7
// Программа считает сумму элементов в каждой строке и выдаёт номер
// строки с наименьшей суммой элементов: 1 строка


// int rows = ReadInt("Введите количество строк: ");
// int colums = ReadInt("Введите количество столбцов: ");
// int[,] numbers = new int[rows, colums];
// FillRandomArray2D(numbers);
// PrintArray2D(numbers);
// Console.WriteLine();
// NumberRowMinSumElementsArray2D(numbers);

// // Функция заполнения массива рандомными числами от 1 до 9
// void FillRandomArray2D(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             array[i, j] = new Random().Next(1, 10);
//         }
//     }
// }

// // Функция вывода двумерного массива
// void PrintArray2D(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             Console.Write(array[i, j] + " ");
//         }
//         Console.WriteLine();
//     }
// }

// // Функция вывода номера строки с наименьшей суммой элементов 
// void NumberRowMinSumElementsArray2D(int[,] array)
// {
//     int minRow = 0;
//     int minSumRow = 0;
//     int sumRow = 0;
//     for (int i = 0; i < array.GetLength(1); i++)
//     {
//         minRow += array[0, i];
//     }
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++) sumRow += array[i, j];
//         if (sumRow < minRow)
//         {
//             minRow = sumRow;
//             minSumRow = i;
//         }
//         sumRow = 0;
//     }
//     Console.Write($"{minSumRow + 1} строка");
// }

// int ReadInt(string message)
// {
//     Console.Write(message);
//     return Convert.ToInt32(Console.ReadLine());
// }


// Задача 58: Задайте две матрицы. Напишите программу, которая 
// будет находить произведение двух матриц.
// Например, даны 2 матрицы:
// 2 4 | 3 4
// 3 2 | 3 3
// Результирующая матрица будет:
// 18 20
// 15 18


// int a = ReadInt("Введите количество строк 1-й матрицы: ");
// int b = ReadInt("Введите количество столбцов 1-й матрицы : ");
// int c = ReadInt("Введите количество строк 2-й матрицы: ");
// int d = ReadInt("Введите количество столбцов 2-й матрицы : ");

// int[,] numbers1 = new int[a, b];
// CreateArray(numbers1);
// Console.WriteLine($"Первая матрица:");
// WriteArray(numbers1);

// int[,] numbers2 = new int[c, d];
// CreateArray(numbers2);
// Console.WriteLine($"Вторая матрица:");
// WriteArray(numbers2);

// int[,] numbers3 = new int[a, d];
// MultiplyMatrix(numbers1, numbers2, numbers3);
// Console.WriteLine($"Произведение первой и второй матриц:");
// WriteArray(numbers3);

// void MultiplyMatrix(int[,] numbers1, int[,] numbers2, int[,] numbers3)
// {
//   for (int i = 0; i < numbers3.GetLength(0); i++)
//   {
//     for (int j = 0; j < numbers3.GetLength(1); j++)
//     {
//       int sum = 0;
//       for (int k = 0; k < numbers1.GetLength(1); k++)
//       {
//         sum += numbers1[i,k] * numbers2[k,j];
//       }
//       numbers3[i,j] = sum;
//     }
//   }
// }

// void CreateArray(int[,] array)
// {
//   for (int i = 0; i < array.GetLength(0); i++)
//   {
//     for (int j = 0; j < array.GetLength(1); j++)
//     {
//       array[i, j] = new Random().Next(1, 10);
//     }
//   }
// }

// void WriteArray (int[,] array)
// {
//   for (int i = 0; i < array.GetLength(0); i++)
//   {
//     for (int j = 0; j < array.GetLength(1); j++)
//     {
//       Console.Write(array[i,j] + " ");
//     }
//     Console.WriteLine();
//   }
// }

// int ReadInt(string message)
// {
//     Console.Write(message);
//     return Convert.ToInt32(Console.ReadLine());
// }



// Задача 60. ...Сформируйте трёхмерный массив из неповторяющихся 
// двузначных чисел. Напишите программу, которая будет построчно 
// выводить массив, добавляя индексы каждого элемента.
// Массив размером 2 x 2 x 2
// 66(0,0,0) 25(0,1,0)
// 34(1,0,0) 41(1,1,0)
// 27(0,0,1) 90(0,1,1)
// 26(1,0,1) 55(1,1,1)


// int rows = ReadInt("Введите количество строк: ");
// int colums = ReadInt("Введите количество столбцов: ");
// int page = ReadInt("Введите количество страниц элементов: ");
// int[,,] array3D = new int[rows, colums, page];
// FillArray(array3D);
// PrintIndex(array3D);

// // Функция вывода индекса элементов 3D массива
// void PrintIndex(int[,,] arr)
// {
//     for (int i = 0; i < array3D.GetLength(0); i++)
//     {        
//         for (int j = 0; j < array3D.GetLength(1); j++)
//         {
//             Console.WriteLine();
//             for (int k = 0; k < array3D.GetLength(2); k++)
//             {
//                 Console.Write($"{array3D[i, j, k]}({i},{j},{k}) ");
//             }
//         }
//     }
// }

// // Функция заполнения 3D массива не повторяющимеся числами
// void FillArray(int[,,] arr)
// {
//     int count = 10;
//     for (int i = 0; i < arr.GetLength(0); i++)
//     {
//         for (int j = 0; j < arr.GetLength(1); j++)
//         {
//             for (int k = 0; k < arr.GetLength(2); k++)
//             {                
//                 arr[k, i, j] += count;
//                 count += 3;                
//             }
//         }
//     }
// }

// int ReadInt(string message)
// {
//     Console.Write(message);
//     return Convert.ToInt32(Console.ReadLine());
// }



// Задача 62. Напишите программу, которая заполнит спирально массив 4 на 4.
// Например, на выходе получается вот такой массив:
// 01 02 03 04
// 12 13 14 05
// 11 16 15 06
// 10 09 08 07


// int n = 4;
// int[,] Matrix = new int[n, n];

// int temp = 1;
// int i = 0;
// int j = 0;

// while (temp <= Matrix.GetLength(0) * Matrix.GetLength(1))
// {
//   Matrix[i, j] = temp;
//   temp++;
//   if (i <= j + 1 && i + j < Matrix.GetLength(1) - 1)
//     j++;
//   else if (i < j && i + j >= Matrix.GetLength(0) - 1)
//     i++;
//   else if (i >= j && i + j > Matrix.GetLength(1) - 1)
//     j--;
//   else
//     i--;
// }

// PrintArray(Matrix);
// void PrintArray(int[,] array)
// {
//     for (int i = 0; i < array.GetLength(0); i++)
//     {
//         for (int j = 0; j < array.GetLength(1); j++)
//         {
//             if (array[i, j] < 10)
//             {
//                 Console.Write("0" + array[i, j]);
//                 Console.Write(" ");
//             }
//             else Console.Write(array[i, j] + " ");
//         }
//         Console.WriteLine();
//     }
// }