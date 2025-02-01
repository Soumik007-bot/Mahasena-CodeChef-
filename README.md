# Mahasena-CodeChef-
A CodeChef problem with rating of 553!

/*Kattapa, as you all know was one of the greatest warriors of his time. The kingdom of Maahishmati had never lost a battle under him (as army-chief), and the reason for that was their really powerful army, also called as Mahasena.

Kattapa was known to be a very superstitious person. He believed that a soldier is "lucky" if the soldier is holding an even number of weapons, and "unlucky" otherwise. He considered the army as "READY FOR BATTLE" if the count of "lucky" soldiers is strictly greater than the count of "unlucky" soldiers, and "NOT READY" otherwise.

Given the number of weapons each soldier is holding, your task is to determine whether the army formed by all these soldiers is "READY FOR BATTLE" or "NOT READY".*/

// https://www.codechef.com/viewsolution/1128261700

#include <stdio.h>

int main() {
    int N, i, Count_E = 0, Count_O = 0;

    scanf("%d", &N);  // Read the number of elements
    
    int S[N];  // Correctly declare array

    for (i = 0; i < N; i++) {
        scanf("%d", &S[i]);  // Read the elements
    }

    for (i = 0; i < N; i++) {
        if (S[i] % 2 == 0) {
            Count_E++;  // Increment even count
        } else {
            Count_O++;  // Increment odd count
        }
    }

    if (Count_E > Count_O) {
        printf("READY FOR BATTLE\n");
    } else {
        printf("NOT READY\n");
    }

    return 0;
}
