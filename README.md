# SequenciaFibonacci
Algoritmo que calcula a sequência de Fibonacci e mostra se o número faz parte desta sequência

    internal class Program
        {
            static void Main(string[] args)
            {
                
                Console.WriteLine("Digite um número para verificar se faz parte da sequência de Fibonacci:");
                int numero = int.Parse(Console.ReadLine());
    
                // armazenamento os dois últimos números da sequência de Fibonacci
                int fibAnterior = 0;
                int fibAtual = 1;
    
                // mostra se o número faz parte da sequência de Fibonacci
                bool fazParte = false;
    
                // mostra a sequência de Fibonacci até encontrar um número maior ou igual ao fornecido pelo usuário
                Console.WriteLine("Sequência de Fibonacci:");
                while (fibAtual <= numero)
                {
                    Console.WriteLine(fibAtual);
    
                    // verifica se o número fornecido está na sequência de Fibonacci
                    if (fibAtual == numero)
                    {
                        fazParte = true;
                        break; // interrompe o loop, pois o número foi encontrado na sequência
                    }
    
                    // atualiza os dois últimos números da sequência de Fibonacci
                    int proximo = fibAnterior + fibAtual;
                    fibAnterior = fibAtual;
                    fibAtual = proximo;
                }
    
                // verifica se o número fornecido faz parte da sequência de Fibonacci
                if (fazParte)
                {
                    Console.WriteLine("\nO número " +numero + "faz parte da sequência de Fibonacci.");
                }
                else
                {
                    Console.WriteLine("\nO número " +numero+ " não faz parte da sequência de Fibonacci.");
                }
    
                Console.ReadLine(); 
            }
        }
