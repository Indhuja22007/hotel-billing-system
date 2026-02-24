#include <stdio.h>

int main() {
    int choice;
    int quantity;
    float total = 0, price;
    char more;

    printf("\n====== WELCOME TO HOTEL FOOD BILLING SYSTEM ======\n");

    do {
        printf("\n-------------- MENU --------------\n");
        printf("1. Burger        - 120 Rs\n");
        printf("2. Pizza         - 250 Rs\n");
        printf("3. Pasta         - 180 Rs\n");
        printf("4. Sandwich      - 100 Rs\n");
        printf("5. Coffee        - 80 Rs\n");
        printf("-----------------------------------\n");

        printf("Enter your choice (1-5): ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                price = 120;
                break;
            case 2:
                price = 250;
                break;
            case 3:
                price = 180;
                break;
            case 4:
                price = 100;
                break;
            case 5:
                price = 80;
                break;
            default:
                printf("Invalid choice!\n");
                price = 0;
        }

        if(price != 0) {
            printf("Enter quantity: ");
            scanf("%d", &quantity);
            total += price * quantity;
            printf("Item added to bill!\n");
        }

        printf("Do you want to order more? (y/n): ");
        scanf(" %c", &more);

    } while(more == 'y' || more == 'Y');

    float tax = total * 0.05;  // 5% tax
    float grandTotal = total + tax;

    printf("\n============= BILL =============\n");
    printf("Total Amount  : Rs %.2f\n", total);
    printf("GST (5%%)      : Rs %.2f\n", tax);
    printf("Grand Total   : Rs %.2f\n", grandTotal);
    printf("================================\n");
    printf("Thank you! Visit Again 😊\n");

    return 0;
}
