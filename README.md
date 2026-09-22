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
            Double mayor, menor, promedio = 0, pares = 0, impares = 0;


            Double maximo = Double.Parse(Console.ReadLine());


            Console.WriteLine("Ingrese "+maximo+" numeros enteros para ser analizados");
            //Double numero = Convert.ToDouble(Console.ReadLine());
            mayor = maximo; menor = maximo;
            

            for (Double i = 0; i < maximo; i++)
            {

                Double numero = Convert.ToDouble(Console.ReadLine());

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
            promedio = promedio / maximo;
            Console.WriteLine("El mayor numero ingresado fue " + mayor + ". El menor fue " + menor);
            Console.WriteLine("El promedio de todos los valores fue " + promedio);
            Console.WriteLine("Hubo " + pares + " Numeros Pares, y " + impares + " Numeros Impares");
        }
        static void Main(string[] args)
        {

            Console.WriteLine("Cuantos numeros desea ingresar?");
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

//7) 

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
            

            int factorPrimo = 0, contador = 0;
            int numero = int.Parse(Console.ReadLine());


            for (int i = 2; factorPrimo != 1; i++)
            {
                while (numero % i == 0)
                {
                    numero = numero / i;
                    factorPrimo = numero;

                    Console.WriteLine(factorPrimo);
                    contador++;
                }                              
            }
            Console.WriteLine("El numero tiene " + contador + " factores primos");

        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese un numero entero para descomponerlo en factores primos");
            NumeradorPrimo();
            
        }
        //
    }
}

// 8) TERMINADO AL FIN POR FAVOR


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
            int NumeroInicial = int.Parse(Console.ReadLine());
            Console.WriteLine("Ingrese el numero que represente el extremo final");
            int NumeroFinal = int.Parse(Console.ReadLine());

            int PrimosTotales = 0, faltas = 0;             

            for(int i = (NumeroInicial + 1); i < NumeroFinal; i++)
            {
                Console.WriteLine(i+" Numero actual ");

                for(int z = 2; z < i; z++)
                {                   
                    Console.WriteLine(z + " Divisor ");

                    if (i % z == 0)
                    {
                        Console.WriteLine("Resultado: " + i % z);
                        faltas += 1;
                        Console.WriteLine(faltas + " falta ");
                    }                
                }
                if(faltas==0)
                {
                    PrimosTotales += 1;
                    Console.WriteLine(" Primos Totales encontrados: " + PrimosTotales);
                    Console.WriteLine("Primo encontrado: " + i);                   
                }
                else
                {
                    faltas = 0;
                }

            }
            Console.WriteLine("Primos Totales encontrados: "+ PrimosTotales);
            ///

        }
        static void Main(string[] args)
        {
            Console.WriteLine("Ingrese un numero que represente el extremo inicio");

            NumeradorPrimo();

        }
        //


    }
}
