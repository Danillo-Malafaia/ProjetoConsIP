#include<stdio.h>
#include<stdlib.h>

//talvez usar isso para criar a biblioteca "meuprojeto.h" ou simplesmente jogar as estruturas no codigo

//lembrar de depois reorganizar as variaveis para deixar o codigo o mais legivel possivel

//ATENÇÃO: obviamente sintam-se livres para alterar e corrigir o codigo, só pessoa que passe um feedback para que o desenvolvimento fique mais dinamico

typedef struct
{
	//se necessario, otimizar o tamanho do vetor para poupar memoria
	char pais[30];
	char estado[20];
	char cidade[20];
	char bairro[20];
	char rua[50];
	char cep[8]; //o numero de digitos padrão de cep
	
}Endereco;

/*typedef struct //ATENÇÂO:eu não vi isso nos requisitos então acredito que a gente pode ignorar o fabricante
{
	
	char nome[30];
	char cnpj[14]; //o numero de digitos padrão de cnpj (para o brasil)
	Endereco;
	
}Fabricante;*/

typedef struct
{
	
	char nome[30];
	char cpf[11]; //o numero de digitos padrão de cpf (para o brasil)
	//Endereco; //está dando erro
	
}Cliente;

typedef struct
{
	
	char nome[30];
	char cpf[11]; //o numero de digitos padrão de cpf (para o brasil)
	float salario; //talvez seja mais interessante por o salario em uma estrutura (já que o salario pode ser por comissão ou qualquer outra variante)
	//Endereco; //está dando erro
	
}Funcionario;

typedef struct
{
	
	char modelo[30];
	char numero_chassi[17]; //17 caracteres é o temanho padrão do numero do chassi
	char ano[4]; //procurar uma forma mais eficiente de por esta informação
	float perco_compra; //não tenho certeza se o preço entra aqui
	float preco_venda; //não tenho certeza se o preço entra aqui
	//Fabricante; //não será implementado se não usarmos o fabricante
		
}Carro;

typedef struct
{
	
	char tipo[30];
	char modelo[30];
	char num_serie[30]; //não faço ideia do tamanho do numero de serie de uma peça de carro (considerando que exitem varios tipos e modelos de peça)
	float perco_compra; //não tenho certeza se o preço entra aqui
	float preco_venda; //não tenho certeza se o preço entra aqui
	//Fabricante; //não será implementado se não usarmos o fabricante
	
}Pecas;

//----------------------------------------------------------------------------------------- (Ainda não tem nada sobre Login e Senha)

//Cadastro (insersão, remoção, busca e edição) Funcionarios, peças e clientes

main()
{
	int verif1=1; //talvez seja mais interessante alterar o nome desta variavel
	int verif2=1; //talvez seja mais interessante alterar o nome desta variavel
	
	do
	{
		printf("Digite 1 se deseja fazer ir para cadastros. Digite 2 se deseja verificar relatorios\n");
		scanf("%i", &verif1);
		
		//verificação das opções (otimizar isso) NOTA: do jeito que está funciona, mas se um caracter for digitado o programa dá erro (resolver isto)
		while (verif1<1)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif1);
			
			while (verif1>2)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif1);
			}
		}
		while (verif1>2)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif1);
			
			while (verif1<1)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif1);
			}
		}

		//implementação das opções (ATENÇÂO:o programa em si provavelmente vai estar dentro de todo esse switch)<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
		switch (verif1)
		{
			case 1:
				printf("teste1\n\n"); //Cadastro (Insersão, remoção, busca e edição) de funcionarios, clientes, carros e peças.
				break;
			case 2:
				printf("teste2\n\n"); //Relatorios (carros mais vendidos, funcionario do mês, faturamento (custo e lucros), clientes que mais consomem
				break;
		}
		
		//verificação da continuidade do programa (otimizar isso) NOTA: do jeito que está funciona, mas se um caracter for digitado o programa dá erro (resolver isto)
		printf("deseja realizar mais alguma operacao? (digite 1 para sim e 0 para nao)\n");
		scanf("%i", &verif2);
			
		while (verif2<0)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif2);
				
			while (verif2>1)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif2);
			}
		}
		while (verif2>1)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif2);
				
			while (verif2<0)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif2);
			}
		}		
	}while (verif2!=0);
}
