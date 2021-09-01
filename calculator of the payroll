#include <stdio.h>
#include <string.h>
//questo 2 - calcular folha de pagamento
typedef struct {  int matricula, cargo, sexo, anosExp, qFilhos;
                  char nome[20];
                  float salario;
} Empregados;

int main(void) {
  int cadNovo = 1;
  int empN = 0;

  Empregados empregado[20];

  while (cadNovo == 1) {

    setbuf(stdin, 0);
    printf("\nEmpresa Legal\n");
    printf("\nCadastro de Funcionario\n");
    printf("\nMatricula: ");
    scanf("%d", &empregado[empN].matricula);

    setbuf(stdin, 0);
    printf("Nome: ");
    fgets(empregado[empN].nome, 20, stdin);
    empregado[empN].nome[strcspn(empregado[empN].nome, "\n")] = '\0';

    do {
      printf("Cargo ( 1 - Analista de Sistemas, 2 - Programador): ");
      scanf("%d", &empregado[empN].cargo);
      if (empregado[empN].cargo < 1 || empregado[empN].cargo > 2) {
        printf("\nInforme um valor valido!\n");
      }

    } while (empregado[empN].cargo < 1 || empregado[empN].cargo > 2);

    do {
      printf("Sexo ( 1 - mas / 2 - fem): ");
      scanf("%d", &empregado[empN].sexo);  
      if (empregado[empN].sexo < 1 || empregado[empN].sexo > 2) {
          printf("\nInforme um valor valido!\n");
      }
    } while (empregado[empN].sexo < 1 || empregado[empN].sexo > 2);

    do {  
      printf("Anos de experiência: ");
      scanf("%d", &empregado[empN].anosExp);
      if (empregado[empN].anosExp < 0) {
        printf("\nO valos não pode ser negativo!\n");
      }
    } while (empregado[empN].anosExp < 0);

    do {
      printf("Quantidade de filhos: ");
      scanf("%d", &empregado[empN].qFilhos);
      if (empregado[empN].qFilhos < 0) {
        printf("\nO valos não pode ser negativo!\n");
      }
    } while (empregado[empN].qFilhos < 0);

    do {
      printf("Cadastrar outro (1 - sim / 2 - não)? ");
      scanf("%d", &cadNovo);
      if (cadNovo < 1 || cadNovo > 2) {
        printf("\nInforme um valor valido\n");
      }
    } while (cadNovo < 1 || cadNovo > 2);

    if (empregado[empN].cargo == 1) {
      empregado[empN].salario = 2500;
    }

    if (empregado[empN].cargo == 2) {
      empregado[empN].salario = 1700;
    }

    empregado[empN].salario += empregado[empN].anosExp * 50;
    empregado[empN].salario += empregado[empN].qFilhos * 40;

    empN++;
  }
  
  printf("\n\nEmpresa Legal\n");
  printf("\nListagem Geral\n");
  printf("┌───────────┬──────────────────────┬──────────────────────┬──────┬──────┬─────────┬────────────┐");
  printf("\n│ Matricula │ Nome                 │ Cargo                │ Sexo | Anos | Q.Filho | Salario    |");
  printf("\n├───────────┼──────────────────────┼──────────────────────┼──────┼──────┼─────────┼────────────┤");

  for(int i = 0; i < empN ; i++) {
  
    printf("\n│ %-9d │ %-20s │ %-20d | %-4d | %-4d | %-7d | %-10.2f |", empregado[i].matricula, empregado[i].nome, empregado[i].cargo , empregado[i].sexo, empregado[i].anosExp, empregado[i].qFilhos, empregado[i].salario );
    
  }

  printf("\n└───────────┴──────────────────────┴──────────────────────┴──────┴──────┴─────────┴────────────┘");

  printf("\n\nEmpresa Legal\n");
  printf("\nListagem Geral\n");
  printf("┌───────────┬──────────────────────┬──────────────────────┬────────────┬──────┬─────────┬────────────┐");
  printf("\n│ Matricula │ Nome                 │ Cargo                │ Sexo       | Anos | Q.Filho | Salario    |");
  printf("\n├───────────┼──────────────────────┼──────────────────────┼────────────┼──────┼─────────┼────────────┤");
  for(int i = 0; i < empN ; i++) {
    char sexo[10];
    char cargo[20];

    if(empregado[i].sexo == 1) {
      strcpy(sexo, "Masculino");
    }
    if(empregado[i].sexo == 2) {
      strcpy(sexo, "Feminino");
    }
    if(empregado[i].cargo == 1) {
      strcpy(cargo, "Analista de Sistemas");
    }
    if(empregado[i].cargo == 2) {
      strcpy(cargo, "Programador");
    }
  
  
    printf("\n│ %-9d │ %-20s │ %-20s | %-10s | %-4d | %-7d | %-10.2f |", empregado[i].matricula, empregado[i].nome, cargo , sexo, empregado[i].anosExp, empregado[i].qFilhos, empregado[i].salario );
  }

  printf("\n└───────────┴──────────────────────┴──────────────────────┴────────────┴──────┴─────────┴────────────┘");
  
}
