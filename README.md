# hotel-billing-system
#include <stdio.h>

int main() {
    int choice, qty;
    float total = 0;

    printf("====== HOTEL BILLING SYSTEM ======\n");
    printf("1. Idli       - Rs.20\n");
    printf("2. Dosa       - Rs.40\n");
    printf("3. Poori      - Rs.35\n");
    printf("4. Tea        - Rs.10\n");
    printf("5. Coffee     - Rs.15\n");
    printf("6. Exit\n");

    while (1) {
        printf("\nEnter your choice: ");
        scanf("%d", &choice);

        if (choice == 6)
            break;

        printf("Enter quantity: ");
        scanf("%d", &qty);

        switch (choice) {
            case 1: total += 20 * qty; break;
            case 2: total += 40 * qty; break;
            case 3: total += 35 * qty; break;
            case 4: total += 10 * qty; break;
            case 5: total += 15 * qty; break;
            default:
                printf("Invalid choice!");
        }
    }

    printf("\n----------------------------");
    printf("\nTotal Bill = Rs.%.2f", total);
    printf("\nThank You! Visit Again 😊");
    printf("\n----------------------------");

    return 0;
}
