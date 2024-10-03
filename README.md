#include <stdio.h>

int main() {
    int age, couponCode;

    printf("Enter your age: ");
    scanf("%d", &age);

    while (age < 18 || age > 30) {
        printf("Error: Age must be between 18 and 30. Please enter again: ");
        scanf("%d", &age);
    }

    printf("Enter your coupon code (0 or 1): ");
    scanf("%d", &couponCode);

    while (couponCode != 0 && couponCode != 1) {
        printf("Invalid coupon code. Please enter 0 or 1: ");
        scanf("%d", &couponCode);
    }

    if (couponCode == 1) {
        printf("Congratulations! You have won the coupon.\n");
        printf("You get a loan without interest.\n");
    } else {
        printf("You have lost the coupon.\n");
        printf("You get a loan with some interest.\n");
    }

    return 0;
}
