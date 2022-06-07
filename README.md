#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int contador(char z[]){
    char letras[] = "abcdefghijklmnopqrstuvwxyz";
    int numero=0,i=0,j=0;
    for(i=0;i<strlen(z);i++){
        for(j=0;j<strlen(letras);j++){
            if(z[i]==letras[j]){
                numero++;
            }
        }
    }
    return (numero);
}



int main()
{
    struct palavras{
    char a[50];
    char b[50];
    char c[50];
    char d[50];
    char e[50];
    };

    struct dicas{
    char v[50];
    char w[50];
    char x[50];
    char y[50];
    char z[50];
    };

    char resposta[50];
    int k=0, conta=0, contb=0, contc=0, contd=0, conte=0;

    struct palavras palavra;
    printf("insira a palavra 1\n");
    fflush(stdin);
    fgets(palavra.a, 40, stdin);
    conta = contador(palavra.a);
    printf("insira a palavra 2\n");
    fflush(stdin);
    fgets(palavra.b, 40, stdin);
    contb = contador(palavra.b);
    printf("insira a palavra 3\n");
    fflush(stdin);
    fgets(palavra.c, 40, stdin);
    contc = contador(palavra.c);
    printf("insira a palavra 4\n");
    fflush(stdin);
    fgets(palavra.d, 40, stdin);
    contd = contador(palavra.d);
    printf("insira a palavra 5\n");
    fflush(stdin);
    fgets(palavra.e, 40, stdin);
    conte = contador(palavra.e);

    struct dicas dica;
    printf("\ninsira a dica da palavra 1\n");
    fflush(stdin);
    fgets(dica.v, 40, stdin);
    printf("insira a dica da palavra 2\n");
    fflush(stdin);
    fgets(dica.w, 40, stdin);
    printf("insira a dica da palavra 3\n");
    fflush(stdin);
    fgets(dica.x, 40, stdin);
    printf("insira a dica da palavra 4\n");
    fflush(stdin);
    fgets(dica.y, 40, stdin);
    printf("insira a dica da palavra 5\n");
    fflush(stdin);
    fgets(dica.z, 40, stdin);
    system("pause");
    system("cls");

    char jogo[30][30];
    int i=0, j=0;
    for (i=0; i<=29; i++){
        for (j=0; j<=29; j++){
            jogo[i][j] = '_';
        }
    }

    for (i=0; i<=0; i++){
        for (j=0; j<=conta; j++){
            jogo[i][j] = palavra.a[j];
            jogo[i][conta] = '_';
        }
    }

    for (i=3; i<=3; i++){
        for (j=0; j<=contb; j++){
            jogo[i][j] = palavra.b[j];
            jogo[i][contb] = '_';
        }
    }


    for (i=0;i<=contc; i++){
        for (j=20; j<=20; j++){
            jogo[i][j] = palavra.c[i];
            jogo[contc][j] = '_';
        }
    }

    palavra.d[j] = palavra.d[j+10];
    for (i=15; i<=15; i++){
        for (j=10; j<=contd+10; j++){
            jogo[i][j] = palavra.d[j+10];
        }
    }





























    for (i=0; i<=29; i++){
        for (j=0; j<=29; j++){
            printf("%c ", jogo[i][j]);
        }
        printf("\n");
    }

    printf("dica 1: %s\n", dica.v);

    printf("dica 2: %s\n", dica.w);

    printf("dica 3: %s\n", dica.x);

    printf("dica 4: %s\n", dica.y);

    printf("dica 5: %s\n", dica.z);

    printf("\n%i\n", conta);
    printf("\n%i\n", contb);
    printf("\n%i\n", contc);
    printf("\n%i\n", contd);
    printf("\n%i\n", conte);


    while (k < 5){
    printf("por favor, insira a palavra de alguma dica\n");
    scanf("%s", &resposta);
    if (resposta == palavra.a, 40, stdin){
        printf("voce acertou a palavra 1\n");
    } else if (resposta == palavra.b, 40, stdin){
        printf("voce acertou a palavra 2\n");
    } else if (resposta == palavra.c, 40, stdin){
        printf("voce acertou a palavra 3\n");
    } else if (resposta == palavra.d, 40, stdin){
        printf("voce acertou a palavra 4\n");
    } else if (resposta == palavra.e, 40, stdin){
        printf("voce acertou a palavra 5\n");
    }
    }
    printf("\nvoce ganhou o jogo seu arrombado");
    return 0;
}
