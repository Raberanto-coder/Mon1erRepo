#include <stdio.h>
#include <math.h>

float Resolution (int a, int b, int c)
{
    float delta, delta0, re, im, x1, x2, x;
    delta = b*b - 4*a*c;
    if (delta<0)
    {
        delta0 = delta*(-1);
        re = (-b)/2*a;
        im = sqrt(delta0)/2*a;
        printf("\nSolutions :\n");

        if (re==0)
        {
            printf(" x1 = i %f\n", im);
            printf(" x2 = - i %f\n", im);
        }
        else
        {
            printf("x1 = %f", re);
            printf(" + i %f\n", im);
            printf("x2 = %f", re);
            printf(" - i %f\n", im);
        }
    }
    else if (delta>0)
    {
        x1 = (-b + sqrt(delta))/2*a;
        x2 = (-b - sqrt(delta))/2*a;
        printf("\nSolutions :\n");
        printf("x1 = %f\n",x1);
        printf("x2 = %f\n",x2);
    }
    else
    {
        x = -b/2*a;
        printf("\nSolution :\n");
    }
    return 0;
}

int main()
{
    int a, b, c;
    float y;
    // résolution d'équation second dégré
    printf("Enter a : ");
    scanf("%d",&a);
    printf("Enter b : ");
    scanf("%d",&b);
    printf("Enter c : ");
    scanf("%d",&c);
    y = Resolution(a, b, c);
    return 0;
}
