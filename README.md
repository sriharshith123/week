#include <stdio.h>

int main() {
    float chennai[7], delhi[7], haveri[7], gangtok[7];
    float chennai_temp;
    int i;

    // Get the temperature of Chennai for the week
    printf("Enter the temperature of Chennai (in degrees Celsius) for the week:\n");
    for (i = 0; i < 7; i++) {
        printf("Day %d: ", i+1);
        scanf("%f", &chennai[i]);
        if (chennai[i] < 28 || chennai[i] > 33) {
            printf("Invalid temperature! Temperature should be between 28C and 33C.\n");
            return 0;
        }
    }

    // Calculate the temperature of Delhi and Haveri for the week
    for (i = 0; i < 7; i++) {
        delhi[i] = chennai[i] - 8;
        haveri[i] = chennai[i] + 5;
    }

    // Calculate the temperature of Gangtok for the week
    for (i = 0; i < 7; i++) {
        gangtok[i] = haveri[i] - delhi[i];
    }

    // Display the temperature of Gangtok for the week
    printf("\nTemperature of Gangtok (in degrees Celsius) for the week:\n");
    for (i = 0; i < 7; i++) {
        printf("Day %d: %.2f\n", i+1, gangtok[i]);
    }

    return 0;
}
