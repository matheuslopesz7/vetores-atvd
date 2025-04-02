#include <stdio.h>

void encontrarSoma(int vetor[], int tamanho, int alvo) {
for (int i = 0; i < tamanho; i++) {
for (int j = i + 1; j < tamanho; j++) {
if (vetor[i] + vetor[j] == alvo) {
printf("Os valores %d (posição %d) e %d (posição %d) somam %d\n",
vetor[i], i, vetor[j], j, alvo);
return;
}
}
}
printf("Nenhuma combinação encontrada que some %d.\n", alvo);
}

int main() {
int vetor[] = {10, 20, 35, 50, 75};
int tamanho = sizeof(vetor) / sizeof(vetor[0]);
int alvo = 55;

encontrarSoma(vetor, tamanho, alvo);

return 0;
}
