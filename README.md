# Classificação de Triângulos
/* Nome: Guilherme Malta*/
Escreva um algoritmo em Java que solicite ao 
usuário a entrada de 3 números. Considere que
estes números são os lados de um triângulo.

Seu algoritmo deverá:

1. Indicar se "realmente" são lados de um triângulo
2. Se os lados compõem um triângulo, identifique 
   qual sua classificação: 
   - Equilátero
   - Isósceles
   - Escaleno

Sua resposta deverá ser enviada através de um PULL REQUEST
a este repositório.

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {

		int valor1, valor2, valor3;

		Scanner sc = new Scanner(System.in);

		System.out.println("Digite o primeiro valor");
		valor1 = sc.nextInt();

		System.out.println("Digite o segundo valor");
		valor2 = sc.nextInt();

		System.out.println("Digite o terceiro valor");
		valor3 = sc.nextInt();

		if ((valor1 == valor2) && (valor2 == valor3)) {
			System.out.println("O triangulo será um Equilatero");
		} else {
			if ((valor1 == valor2) && (valor2 != valor3) || (valor1 != valor2) && (valor2 == valor3)
					|| (valor1 != valor2) && (valor1 == valor3)) {
				System.out.println("O triangulo será é Isóceles");
			} else {
				if ((valor1 != valor2) && (valor1 != valor3)) {
					System.out.println("O triangulo será um Escaleno");
				}
			}

		}

	}

}

