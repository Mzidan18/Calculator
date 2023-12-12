#include <stdio.h>

int main() {
    char operator;
    double bilangan1, bilangan2, hasil;
    
    printf("\t\t\tUNIVERSITAS NEGERI PADANG\n\n"); //Nama Universitas
    printf("==========================================\n");
    printf("Nama : M Zidan\n NIM  : 23346011\n"); //Identitas
    printf("==========================================\n");
    printf("Program Kalkulator \n \n"); //Nama Program
    printf("==========================================\n");


    printf("Masukkan operator (+, -, *, /): ");
    scanf(" %c", &operator);

    printf("Masukkan dua bilangan: ");
    scanf("%lf %lf", &bilangan1, &bilangan2);

    switch(operator) {
        case '+':
            hasil = bilangan1 + bilangan2;
            printf("Hasil penjumlahan: %.2lf\n", hasil);
            break;
        case '-':
            hasil = bilangan1 - bilangan2;
            printf("Hasil pengurangan: %.2lf\n", hasil);
            break;
        case '*':
            hasil = bilangan1 * bilangan2;
            printf("Hasil perkalian: %.2lf\n", hasil);
            break;
        case '/':
            if(bilangan2 != 0) {
                hasil = bilangan1 / bilangan2;
                printf("Hasil pembagian: %.2lf\n", hasil);
            } else {
                printf("Tidak dapat melakukan pembagian dengan nol.\n");
            }
            break;
        default:
            printf("Operator yang dimasukkan tidak valid.\n");
    }

    return 0;
}

