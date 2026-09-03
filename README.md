# Funciones-2-La-venganza

//1)

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {

        static void Numerador()
        {
            //mayor, menor, promedio de todos, cantidad impares y pares
            int mayor, menor, promedio = 0, pares = 0, impares = 0;

            int numero = Convert.ToInt32(Console.ReadLine());
            mayor = numero; menor = numero;
            promedio += numero;

            for (int i = 0; i < 4; i++)
            {

                numero = int.Parse(Console.ReadLine());

                promedio = promedio + numero;

                if (numero < menor) 
                {
                    menor = numero;
                }
                if (numero > mayor)
                {
                    mayor = numero;
                }
                if (numero % 2 == 0)
                {
                    pares += 1;
                }
                else if (numero % 2 != 0) 
                {
                    impares += 1;
                }
                
            }
            promedio = promedio / 5;
            Console.WriteLine("El mayor numero ingresado fue "+mayor+". El menor fue "+menor);
            Console.WriteLine("El promedio de todos los valores fue "+promedio);
            Console.WriteLine("Hubo "+pares+" Numeros Pares, y "+impares+" Numeros Impares");
        }
        static void Main(string[] args)
        {

            Console.WriteLine("Ingrese 5 numeros enteros para ser analizados");
            Numerador();

        }
        //
    }
}

//2)

