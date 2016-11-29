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
	Endereco cliente;
	
}Cliente;

typedef struct
{
	
	char nome[30];
	char cpf[11]; //o numero de digitos padrão de cpf (para o brasil)
	float salario; //talvez seja mais interessante por o salario em uma estrutura (já que o salario pode ser por comissão ou qualquer outra variante)
	Endereco funcionario;
	
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
		printf("Digite 1 se deseja fazer ir para cadastros. Digite 2 se deseja verificar relatorios. Digite qualquer outro numero se deseja sair\n");
		scanf("%i", &verif1);
		
		//Esses Whiles curzados provavelmente são apenas lixo (ELIMINAR CASO NÃO UTILIZAR)<<<<<<

		//verificação das opções (otimizar isso) NOTA: do jeito que está funciona, mas se um caracter ou um numero float for digitado o programa dá erro (resolver isto)
		/*while (verif1<1)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif1);
			
			while (verif1>3)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif1);
			}
		}
		while (verif1>3)
		{
			printf ("Esta opcao eh invalida, por favor digite outro numero\n");
			scanf("%i", &verif1);
			
			while (verif1<1)
			{
				printf ("Esta opcao eh invalida, por favor digite outro numero\n");
				scanf("%i", &verif1);
			}
		}*/

		//implementação das opções (ATENÇÂO:o programa em si provavelmente vai estar dentro de todo esse switch)<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
		int menuA=1;
		int menuB=1;
		
		switch (verif1)
		{
			case 1: //CADASTROS--------------------------------------------------------------------
			{
				do
				{
					printf("\nVoce escolheu cadastros. Que tipo de operacao deseja fazer?\n"); //Cadastro (Insersão, remoção, busca e edição) de funcionarios, clientes, carros e peças.
					printf("\n1-carros e pecas\n2-clientes\n3-funcionarios\n\ndigite qualquer outro numero para sair\n");
					scanf("%i", &menuA);
					
					switch(menuA)
					{
						case 1: //Carros e peças<<<<<<<<<<
						{
							int menu1=1;
							
							do
							{
								printf("\nVoce escolheu carros e pecas. Que tipo de opreacao deseja fazer?\n");
								printf("\n1-novo cadastro\n2-remover cadastro\n3-editar cadastro\n4-buscar cadastro\n5-sair\n");
								scanf("%i", &menu1);
								
								switch(menu1)
								{
									case 1:
									{
										//adicionar;
										break;
									}
									case 2:
									{
										//deletar;
										break;
									}
									case 3:
									{
										//editar;
										break;
									}
									case 4:
									{
										//procurar;
										break;
									}
									case 5:
										break;
								}
							}while(menu1!=5);
							break;
						}
						break;
						
						case 2: //Clientes<<<<<<<<<<
						{
							int menu1=1;
							
							do
							{
								printf("\nVoce escolheu clientes. Que tipo de opreacao deseja fazer?\n");
								printf("\n1-novo cadastro\n2-remover cadastro\n3-editar cadastro\n4-buscar cadastro\n5-sair\n");
								scanf("%i", &menu1);
								
								switch(menu1)
								{
									case 1:
									{
										//adicionar;
										break;
									}
									case 2:
									{
										//deletar;
										break;
									}
									case 3:
									{
										//editar;
										break;
									}
									case 4:
									{
										//procurar;
										break;
									}
									case 5:
										break;
								}
							}while(menu1!=5);
							break;
						}
						break;
						
						case 3: //Funcionarios<<<<<<<<<<
						{
							int menu1=1;
							
							do
							{
								printf("\nVoce escolheu funcionarios. Que tipo de opreacao deseja fazer?\n");
								printf("\n1-novo cadastro\n2-remover cadastro\n3-editar cadastro\n4-buscar cadastro\n5-sair\n");
								scanf("%i", &menu1);
								
								switch(menu1)
								{
									case 1:
									{
										//adicionar;
										break;
									}
									case 2:
									{
										//deletar;
										break;
									}
									case 3:
									{
										//editar;
										break;
									}
									case 4:
									{
										//procurar;
										break;
									}
									case 5:
										break;
								}
							}while(menu1!=5);
							break;
						}
						break;
						
						case 4: //Fim do switch<<<<<<<<<<
							break;
					}
					break;
				}while(menuA!=4);
				break;
			}
			
			case 2: //RELATORIOS--------------------------------------------------------------------
			{
				do
				{
					printf("\nVoce escolheu relatorios. Que tipo de operacao deseja fazer?\n"); //Relatorios (carros mais vendidos, funcionario do mês, faturamento (custo e lucros), clientes que mais consomem)
					printf("\n1-carros mais vendidos\n2-funcionario do mes\n3-faturamento\n4-clientes que mais consomem\n\ndigite qualquer outro numero para sair\n");
					scanf("%i", &menuB);
					break;
					
					switch(menuB)
					{
						case 1: //Carros mais vendidos<<<<<<<<<<
						{
							int menu1=1;
							
							do
							{
								printf("\nVoce escolheu carros mais vendidos. Que tipo de opreacao deseja fazer?\n");
								printf("\n1-carros mais vendidos no ultimo mes\n2-carros mais vendido nos ultimos 6 meses\n3-carros mais vendidos neste ano\n4-sair\n");
								scanf("%i", &menu1);
								
								switch(menu1)
								{
									case 1:
									{
										//mais vendidos no ultimo mes;
										break;
									}
									case 2:
									{
										//mais vendidos nos ultimos 6 meses;
										break;
									}
									case 3:
									{
										//mais vendidos neste ano;
										break;
									}
									case 4:
										break;
								}
							}while(menu1!=4);
							break;
						}
						break;
						
						case 2: //Funcionario do mes<<<<<<<<<<
						{
							//Funcionario do mes
							break;
						}
						break;
						
						case 3: //Faturamento<<<<<<<<<<
						{
							int menu1=1;
							
							do
							{
								printf("\nVoce escolheu faturamento. Que tipo de opreacao deseja fazer?\n");
								printf("\n1-faturamento deste mes\n2-faturamento do mes passado\n3-faturamento deste ano(ate agora)\n4-faturamento do ano passado\n5-sair\n");
								scanf("%i", &menu1);
								
								switch(menu1)
								{
									case 1:
									{
										//faturamento deste mes;
										break;
									}
									case 2:
									{
										//faturamento mes passado;
										break;
									}
									case 3:
									{
										//faturamento deste ano;
										break;
									}
									case 4:
									{
										//faturamento ano passado;
										break;
									}
									case 5:
										break;
								}
							}while(menu1!=5);
							break;
						}
						break;
						
						case 4: //Clientes que mais consomem<<<<<<<<<<
						{
							//Lista de clientes que mais consomem
							break;
						}
						break;
						
						case 5: //Fim do switch<<<<<<<<<<
							break;
					}
					break;
				}while(menuB!=5);
				break;
			}
		}
		
		//verificação da continuidade do programa (otimizar isso) NOTA: do jeito que está funciona, mas se um caracter ou numero float for digitado o programa dá erro (resolver isto)
		printf("\ndeseja realizar mais alguma operacao? (digite qualquer numero para sim e 0 para nao)\n");
		scanf("%i", &verif2);
		
		if(verif2==0)
		{
			verif1=3;
		}
			
		//Esses Whiles curzados provavelmente são apenas lixo (ELIMINAR CASO NÃO UTILIZAR)<<<<<<	
		
		/*while (verif2<0)
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
		}*/		
	}while (verif1!=3);
}
