PU1: 40 000 000 000
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

PU4:while + factorial

#include <stdio.h>

int main()
{
    long int a,c,b,ll,n;
    printf("Ievadiet vienu decimāldaļskaitli: ");
    scanf("%ld",&n);
    printf("Izvēlētiet datu tipu(char-c; int-b; long long-ll)\n: ");
    scanf("%ld",&a);
    
    int i,f;
    f=i=1;
    if(a=c, n>=1, n<=12)
        {
         printf("Atvainojiet, ar 'char' datu tipu pareizi aprēķināt faktoriālu nav iespējams\n");
        }
    if(a=ll, n>=1, n<=12)
        {
         printf("Atvainojiet, ar 'long long' datu tipu pareizi aprēķināt faktoriālu nav iespējams\n");
        }
    if(a=b, n>=1, n<=12)
    {
     while(i<=n)
        {
         f*=i;
         i++;
        }
     printf("Faktoriāls no ievadītā skaitļa (%ld) ir : %d",n,f);
    }
    
    if(a=c, n>=13)
        {
         printf("Atvainojiet, ar 'char' datu tipu pareizi aprēķināt faktoriālu nav iespējams\n");
        }
    if(a=ll, n>=13)
        {
         printf("Atvainojiet, ar 'long long' datu tipu pareizi aprēķināt faktoriālu nav iespējams\n");
        }
    if(a=b, n>=13)
    {
     while(n>=13)
        {
         printf("Faktoriāls no ievadītā skaitļa: Faktoriālam nav vērtības\n");
         break;
        }
    }
    return 0;
}



                                                           26.11.2020

 GNU nano 4.9.3                    filie_write.c                               
/* fwrite example: write buffer */
#include <stdio.h>
 
int main ()
{
        FILE *pFile;
        char buffer[] = { 'x', 'y', 'z' };
        pFile = fopen ("myfile.bin", "wb");
        fwrite (buffer, sizeof(char), sizeof(buffer)/sizeof(char), pFile);
        fclose (pFile);
        return 0;
}
localhost:~# gcc filie_write.c
llocalhost:~# ls -lt
total 40
-rwxr-xr-x    1 root     root         18940 Nov 26 17:24 a.out
-rw-r--r--    1 root     root           254 Nov 26 17:24 filie_write.c
-rw-r--r--    1 root     root           151 Jul  5 19:49 readme.txt
-rw-r--r--    1 root     root           114 Jul  5 19:47 bench.py
-rw-r--r--    1 root     root            76 Jul  3 11:15 hello.c
 
localhost:~# cat filie_write.c
/* fwrite example: write buffer */
#include <stdio.h>
 
int main ()
{
        FILE *pFile;
//      char buffer[] = { 'x', 'y', 'z' };
        int buffer[] = {101, 202, 303};
        pFile = fopen ("myfile.bin", "wb");
        fwrite (buffer, sizeof(int), sizeof(buffer)/sizeof(int), pFile);
        fclose (pFile);
        return 0;
}
localhost:~# mv filie_write.c filie_write.c
localhost:~# gcc filie_write.c -o filie_write.out
  GNU nano 4.9.3                    filie_write.c                               
/* fwrite example: write buffer */
#include <stdio.h>
 
int main ()
{
        FILE *pFile;
//      char buffer[] = { 'x', 'y', 'z' };
        int buffer[] = {101, 202, 303};
        pFile = fopen ("myfile.bin", "wb");
//      fwrite (buffer, sizeof(int), sizeof(buffer)/sizeof(int), pFile);
        fwrite (buffer, 1, sizeof(buffer), pFile);
        fclose (pFile);
        return 0;
}                   
                                                30.11.2020/07.01.2021
                                                
http://gnuplot.respawned.com/
# Scale font and line width (dpi) by changing the size! It will always display stretched.
set terminal svg size 400,300 enhanced fname 'arial'  fsize 10 butt solid
set output 'out.svg'

# Key means label...
set title "Intersection of  f(x) = cosh(x/2) D.a: x=R "
set xlabel 'X'
set ylabel 'Y'
set samples 50
set style data points
plot [-7:7] cosh(x/2)
set title 'Some Data'

                                                07.01.2021

 norakstīts uz JSLinux
localhost:~# ls -lt
total 24
-rw-r--r--    1 root     root           300 Jan  7 16:08 data.txt
-rw-r--r--    1 root     root           349 Jan  7 15:59 script1.gp
-rw-r--r--    1 root     root           151 Jul  5  2020 readme.txt
-rw-r--r--    1 root     root           114 Jul  5  2020 bench.py
-rw-r--r--    1 root     root            76 Jul  3  2020 hello.c
-rw-r--r--    1 root     root            22 Jun 26  2020 hello.js
localhost:~# cat script1.gp
# Scale front and line width (dpi) by changing the size! It will always display
stretched.
set terminal svg size 400,300 enhanced fname 'arial' fsize 10butt solid
set output 'out.svg'
 
# Key mens label...
set title "Intersection of f(x) = cosh(x/2) D.a.: x=R"
set xlabel 'X'
set ylabel 'Y'
set samples 50
set style data points
plot [-7:7] cosh(x/2)
