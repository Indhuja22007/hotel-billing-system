#include &lt;stdio.h&gt;
int main() {
int foodChoice, quantity;
float totalBill = 0.0, tax = 0.1, discount = 0.05;
// Displaying the menu
printf(&quot;Hotel Food Billing System\n&quot;);
printf(&quot;Menu:\n&quot;);
printf(&quot;1. Pizza ($10)\n&quot;);
printf(&quot;2. Burger ($5)\n&quot;);
printf(&quot;3. Pasta ($7)\n&quot;);
printf(&quot;4. Salad ($3)\n&quot;);
printf(&quot;5. Exit\n&quot;);
// Read user input for menu selection

do {
printf(&quot;Enter your choice (1-5): &quot;);
scanf(&quot;%d&quot;, &amp;foodChoice);
// Handle food selection
if (foodChoice &gt;= 1 &amp;&amp; foodChoice &lt;= 4) {
printf(&quot;Enter quantity: &quot;);
scanf(&quot;%d&quot;, &amp;quantity);
// Process the food item and update the total bill
switch(foodChoice) {
case 1:
totalBill += 10 * quantity;
break;
case 2:
totalBill += 5 * quantity;
break;
case 3:
totalBill += 7 * quantity;
break;
case 4:
totalBill += 3 * quantity;
break;
}
} else if (foodChoice == 5) {
break;
} else {
printf(&quot;Invalid choice. Please try again.\n&quot;);
}
} while (foodChoice != 5);
// Calculate taxes and discounts
float taxAmount = totalBill * tax;
float discountAmount = totalBill * discount;
// Final bill calculation
totalBill += taxAmount - discountAmount;
// Displaying the final bill
printf(&quot;\nFinal Bill:\n&quot;);
printf(&quot;Total Food Cost: $%.2f\n&quot;, totalBill - taxAmount +
discountAmount);
printf(&quot;Tax (10%%): $%.2f\n&quot;, taxAmount);
printf(&quot;Discount (5%%): -$%.2f\n&quot;, discountAmount);
printf(&quot;Total Bill: $%.2f\n&quot;, totalBill);
return 0;
}
}
