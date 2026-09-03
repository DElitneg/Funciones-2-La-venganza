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

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {

        static void PerfectCell()
        {
            //LA SUMA DE LOS DIVISORES == AL NUMERO (positivos, excluyendo al mismo numero, ej 1 no es Perfecto)

            int numero = int.Parse(Console.ReadLine());
            int suma = 0;

            for (int i = 1; i < numero; i++)
            {
                if(numero%i == 0)
                {
                    suma += i;
                }  
            }
            if(suma == numero)
            {
                Console.WriteLine("El Numero es PERFECTO");
            }
            else
            {
                Console.WriteLine("El numero NO es Perfecto");
            }        

        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese un numero positivo para calcular si es perfecto (sonidos de Cell de fondo)");
            PerfectCell();
        }
        //
    }
}

//3)

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
            //LA SUMA DE LOS DIVISORES == AL NUMERO (positivos, excluyendo al mismo numero, ej 1 no es Perfecto)

            int numeroInicio = int.Parse(Console.ReadLine());

            Console.WriteLine("Ingrese el segundo numero para establecer el final");
            int numeroFinal = int.Parse(Console.ReadLine());


            int suma = 0, pares = 0, impares = 0;

            for (int i = numeroInicio; i <= numeroFinal; i++)
            {
                Console.WriteLine(i);
                suma += i;

                if (i % 2 == 0)
                {
                    pares += 1;
                }
                else if (i % 2 != 0)
                {
                    impares += 1;
                }           
            }
            Console.WriteLine("La suma total de todos los numeros fue de "+suma);
            Console.WriteLine("Hubo "+pares+" Numeros Pares");
            Console.WriteLine("Y hubo "+impares+" Numeros Impares");

        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese el primer numero para establecer el inicio");
            Numerador();
        }
        //
    }
}

//4) 

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
            //negativos,positivos,ceros y el promedio de los positivos y de los negativos
            int positivos = 0, negativos = 0, ceros = 0, promedioNegativo = 0, promedioPositivo = 0;       

            for (int i = 0; i < 10; i++)
            {
                int numero = int.Parse(Console.ReadLine());

                if (numero > 0)
                {
                    positivos += 1;
                    promedioPositivo += numero;
                }
                if (numero < 0)
                {
                    negativos += 1;
                    promedioNegativo += numero;
                }
                if (numero == 0)
                {
                    ceros += 1;
                }
            }
            promedioNegativo /= negativos;
            promedioPositivo /= positivos;
            Console.WriteLine("El promedio de los valores Positivos fue de " + promedioPositivo + ". Y el de los Negativos fue de " + promedioNegativo);
            Console.WriteLine("Hubo " + positivos + " Numeros Positivos, hubo " + negativos + " Numeros Negativos, y hubo "+ceros+" ceros");
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese 5 numeros enteros para ser analizados");
            Numerador();
        }
        //
    }
}

//5)









//6)

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
            //mayor y segundo mayor xdd
            int mayor, segundoMayor;

            int numero = Convert.ToInt32(Console.ReadLine());
            mayor = numero; segundoMayor = numero;

            for (int i = 0; i < 4; i++)
            {

                numero = int.Parse(Console.ReadLine());

                if (numero > mayor)
                {
                    segundoMayor = mayor;
                    mayor = numero;
                }
                else if (numero >segundoMayor)
                {
                    segundoMayor = numero;
                }
            }
            Console.WriteLine("El mayor numero ingresado fue " + mayor);
            Console.WriteLine("El segundo mayor numero ingresado fue " + segundoMayor);
        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese 5 numeros enteros para ser analizados");
            Numerador();

        }
        //
    }
}

//7) Incompleto

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {

        static void NumeradorPrimo()
        {
            //la descomposicion de factores primos es como la potencia pero divisoria

            int factorPrimo = 0;
            int numero = int.Parse(Console.ReadLine());


            for (int i = 2; factorPrimo != 1; i++)
            {
                while (numero % i == 0) 
                {
                    factorPrimo = numero / i;
                }
            }
            Console.WriteLine(factorPrimo);

         }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese un numero entero para descomponerlo en factores primos");
            NumeradorPrimo();

        }
        //
    }
}
