# Insercao-o-Ordenada-em-Vetores
Inserção Ordenada em Vetores
Inserção Ordenada em Vetores  
include <stdio.h>

void inserir_ordenado(int vetor[], int tamanho, int elemento) {
    int i = tamanho - 1;
    
    // Desloca os elementos para a direita até encontrar a posição correta
    while (i >= 0 && vetor[i] > elemento) {
        vetor[i + 1] = vetor[i];
        i--;
    }
    
    // Insere o novo elemento na posição correta
    vetor[i + 1] = elemento;
}

int main() {
    int QTD;
    
    printf("Digite a quantidade de elementos: ");
    scanf("%d", &QTD);
    
    int vetor[QTD];
    
    for (int i = 0; i < QTD; i++) {
        int elemento;
        printf("Digite o %dº elemento: ", i + 1);
        scanf("%d", &elemento);
        
        inserir_ordenado(vetor, i, elemento);
    }
    
    printf("Vetor ordenado: ");
    for (int i = 0; i < QTD; i++) {
        printf("%d ", vetor[i]);
    }
    printf("\n");
    
    return 0;
}
