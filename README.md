# Java---Menu-Interativo-While-Switch-
Projeto em Java criado para praticar lógica de programação e estruturas de controle. O programa utiliza while, switch e Scanner para implementar um menu interativo no console, permitindo ao usuário executar operações simples, como exibir mensagens, ler números, somar valores e encerrar a aplicação de forma controlada. 

import java.util.Scanner;

public class MenuInterativo {

    public static void main(String[] args) {

        Scanner entradas = new Scanner(System.in);
        int opcao = -1;

        while (opcao != 0) {

            System.out.println("===== MENU =====");
            System.out.println("1 - Dizer Olá");
            System.out.println("2 - Mostrar um número");
            System.out.println("3 - Somar dois números");
            System.out.println("0 - Sair");
            System.out.print("Escolha uma opção: ");

            opcao = entradas.nextInt();
            System.out.println();

            switch (opcao) {

                case 1:
                    System.out.println("Olá 😄 Seja bem-vindo!");
                    break;

                case 2:
                    System.out.print("Digite um número: ");
                    int numero = entradas.nextInt();
                    System.out.println("Você digitou: " + numero);
                    break;

                case 3:
                    System.out.print("Digite o primeiro número: ");
                    int num1 = entradas.nextInt();

                    System.out.print("Digite o segundo número: ");
                    int num2 = entradas.nextInt();

                    int resultado = num1 + num2;
                    System.out.println("Resultado da soma: " + resultado);
                    break;

                case 0:
                    System.out.println("Muito obrigado, tenha um ótimo dia! 👋");
                    break;

                default:
                    System.out.println("Opção inválida!");
            }

            System.out.println(); // linha em branco para organizar o menu
        }

        entradas.close();
    }
}
