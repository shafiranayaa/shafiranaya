#include <stdio.h>
#include <stdlib.h>

int main() 
{
    int width, height;

    while (1) {
        printf("Masukkan lebar (10-100): ");
        scanf("%d", &width);
        printf("Masukkan tinggi (5-75): ");
        scanf("%d", &height);

        
        if (width < 10 || width > 100) {
            printf("Lebar tidak valid! Harus antara 10 dan 100.\n");
            continue;
        }
        if (height < 5 || height > 75) {
            printf("Tinggi tidak valid! Harus antara 5 dan 75.\n");
            continue;
        }
        for (int i = 0; i < height; i++) {
        for (int j = 0; j < width; j++) {
            if (i == 0 || i == height - 1 || j == 0 || j == width - 1) {
                printf("*");
            } else {
                printf(" ");
            }
        }
        printf("\n");
    }

    return 0;}
}
