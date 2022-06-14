#include <stdio.h>

int main()
{
    char *month[] = {"January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"};
    char *days[] = {"Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"};
    int monthDay[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
    int i, j, k, n, weekend, spaceCounter = 0;
    printf("\n\nFor which year you want to see Calender: ");
    scanf("%d", &n);
    if ((n % 4 == 0 && n % 100 != 0) || n % 400 == 0)
    {
        monthDay[1] = 29;
    }
    weekend = (n * 365 + ((n - 1) / 4) - ((n - 1) / 100) + ((n - 1) / 400)) % 7;

    printf("\n\n----------------Calender of year:%d------------------\n\n", n);
    for (i = 0; i < 12; i++)
    {
        printf("\n..................%s..................\n\n", month[i]);
        for (j = 0; j < 7; j++)
        {
            printf("   %s", days[j]);
        }
        printf("\n");
        for (spaceCounter = 0; spaceCounter < weekend; spaceCounter++)
        {
            printf("      ");
        }
        for (k = 0; k < monthDay[i]; k++)
        {
            printf("%6d", (k + 1));
            weekend++;
            if (weekend > 6)
            {
                weekend = 0;
                printf("\n");
            }
        }
        printf("\n");
    }
}
