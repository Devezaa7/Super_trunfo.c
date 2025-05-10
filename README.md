# Super_trunfo.c
Criando as Cartas do Super Trunfo
#include <stdio.h>

// Estrutura para armazenar os dados de uma carta
struct Carta {
    char estado;
    char codigo[4];
    char nomeCidade[100];
    int populacao;
    float area;
    float pib;
    int pontosTuristicos;
};

int main() {
    struct Carta carta1, carta2;

    printf("Cadastro da Carta 1:\n");
    printf("Digite o estado (A-H): ");
    scanf(" %c", &carta1.estado);

    printf("Digite o código da carta (ex: A01): ");
    scanf("%s", carta1.codigo);

    printf("Digite o nome da cidade: ");
    getchar(); // Limpa o buffer do teclado antes do fgets
    fgets(carta1.nomeCidade, sizeof(carta1.nomeCidade), stdin);

    // Remover o \n final lido pelo fgets, se houver
    int len = 0;
    while (carta1.nomeCidade[len] != '\0') {
        if (carta1.nomeCidade[len] == '\n') {
            carta1.nomeCidade[len] = '\0';
            break;
        }
        len++;
    }

    printf("Digite a população: ");
    scanf("%d", &carta1.populacao);

    printf("Digite a área em km²: ");
    scanf("%f", &carta1.area);

    printf("Digite o PIB em bilhões de reais: ");
    scanf("%f", &carta1.pib);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &carta1.pontosTuristicos);

    printf("\nCadastro da Carta 2:\n");
    printf("Digite o estado (A-H): ");
    scanf(" %c", &carta2.estado);

    printf("Digite o código da carta (ex: B02): ");
    scanf("%s", carta2.codigo);

    printf("Digite o nome da cidade: ");
    getchar(); // Limpa o buffer
    fgets(carta2.nomeCidade, sizeof(carta2.nomeCidade), stdin);

    len = 0;
    while (carta2.nomeCidade[len] != '\0') {
        if (carta2.nomeCidade[len] == '\n') {
            carta2.nomeCidade[len] = '\0';
            break;
        }
        len++;
    }

    printf("Digite a população: ");
    scanf("%d", &carta2.populacao);

    printf("Digite a área em km²: ");
    scanf("%f", &carta2.area);

    printf("Digite o PIB em bilhões de reais: ");
    scanf("%f", &carta2.pib);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &carta2.pontosTuristicos);

    // Exibição dos dados
    printf("\n=========================\n");
    printf("Carta 1:\n");
    printf("Estado: %c\n", carta1.estado);
    printf("Código: %s\n", carta1.codigo);
    printf("Nome da Cidade: %s\n", carta1.nomeCidade);
    printf("População: %d\n", carta1.populacao);
    printf("Área: %.2f km²\n", carta1.area);
    printf("PIB: %.2f bilhões de reais\n", carta1.p
