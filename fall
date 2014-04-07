using System;
 
class Program
{
    static void Main()
    {
        int[,] matrix = new int[8, 8];
        int nextCell = 0;
        int tempRow = 0;
        int n;
 
        for (int row = 0; row < 8; row++)
        {
            n = Int32.Parse(Console.ReadLine());
            for (int column = 0; column < 8; column++)
            {
                matrix[row, column] = ((n >> column) & 1);
            }
        }
        for (int row = 6; row >= 0; row--)
        {
            for (int column = 0; column < 8; column++)
            {
                if (matrix[row, column] == 1)
                {
                    tempRow = row + 1;
                    while ((tempRow < 8) && (matrix[tempRow, column] != 1))
                    {
                        matrix[tempRow, column] = matrix[tempRow - 1, column];
                        matrix[tempRow - 1, column] = 0;
                        tempRow++;
                    }
                }
            }
        }
        for (int row = 0; row < 8; row++)
        {
            n = 0;
            for (int column = 0; column < 8; column++)
            {
                n+= (int)(Math.Pow(2, column)) * matrix[row, column];
            }
            Console.WriteLine(n);
        }
    }
}
