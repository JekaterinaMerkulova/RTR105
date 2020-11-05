 #include <stdio.h>
int main()
{
    long int a;
    long int b;
    printf("Ievadiet 1. skaitli: ");
    scanf("%ld", &a);
    printf("Ievadiet 2. skaitli: ");
    scanf("%ld", &b);
    printf("%ld * %ld = %ld ", a,b,a*b);
    
    return 0;
}
