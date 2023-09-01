using System;

namespace CalculadoraSimples
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Calculadora Simples");
            Console.WriteLine("1. Adição");
            Console.WriteLine("2. Subtração");
            Console.WriteLine("3. Multiplicação");
            Console.WriteLine("4. Divisão");
            Console.Write("Escolha uma opção: ");

            int escolha = int.Parse(Console.ReadLine());

            Console.WriteLine("Digite o primeiro número: ");
            double numero1 = double.Parse(Console.ReadLine());

            Console.WriteLine("Digite o segundo número: ");
            double numero2 = double.Parse(Console.ReadLine());

            double resultado = 0;

            switch (escolha)
            {
                case 1:
                    resultado = numero1 + numero2;
                    break;
                case 2:
                    resultado = numero1 - numero2;
                    break;
                case 3:
                    resultado = numero1 * numero2;
                    break;
                case 4:
                    if (numero2 != 0)
                    {
                        resultado = numero1 / numero2;
                    }
                    else
                    {
                        Console.WriteLine("O segundo número tem que ser diferente de 0");
                        return;
                    }
                    break;
                default:
                Console.WriteLine("Opção inválida!");
                break;


            }
              
                    Console.WriteLine($"o resultado da {escolha} é {resultado}");

        }
    }
}
