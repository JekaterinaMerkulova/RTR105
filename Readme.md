                           Programmēšanas uzdevumi.

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

    PU2: dec2bin
#include <stdio.h>
int main()
{
 char a[10],n,i;
 printf("Ievadiet vienu decimāldaļskaitli: ");
 scanf("%d",&n);
 for(i=0;n>0;i++)
 {
  a[i]=n%2;
  n=n/2;
 }
 printf("\nBinārais skaitlis no ievadītā ir: ");
 for(i=i-1;i>=0;i--)
 {
  printf("%d",a[i]);
 }
return 0;
} 

    PU3: if + simple sort
#include <stdio.h>
int main()
{
 int skait_1; //Skaitlis Nr.1
 int skait_2; //Skaitlis Nr.2
 int skait_3; //Skaitlis Nr.3
 char s;

 printf("ievadiet skait_1: ");
 scanf("%d", &skait_1);
 printf("ievadiet skait_2: ");
 scanf("%d", &skait_2);
 printf("ievadiet skait_3: ");
 scanf("%d", &skait_3);
 printf("ievadiet skaitlu augošā secībā - a ; dilstošā - d \n");
 scanf("%s", &s);
 
 printf("ja ievaditājs simbols ir a(%d), tad: \n", s=='a');
 if(s=='a')
 {
  if(skait_1>skait_2>skait_3)
  {
    printf("%d %d %d \n", skait_1, skait_2, skait_3);
  }
  else if(skait_3>skait_2>skait_1)
  {
   printf("%d %d %d \n", skait_3, skait_2, skait_1);
  }
  else if(skait_3>skait_1>skait_2)
  {
   printf("%d %d %d \n", skait_3, skait_1, skait_2);
  }
 }
 printf("ja ievaditājs simbols ir d(%d), tad: \n", s=='d');
 if(s=='d')
 {
  if(skait_1<skait_2<skait_3)
  {
   printf("%d %d %d \n", skait_1, skait_2, skait_3);
  }
  else if(skait_3<skait_2<skait_1)
  {
   printf("%d %d %d \n", skait_3, skait_2, skait_1);
  }
  else if(skait_3<skait_1<skait_2)
  {
   printf("%d %d %d \n", skait_3, skait_1, skait_2);
  }
 }
return 0;
}

    PU4: while + factorial
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

    PU5: for + factorial
#include <stdio.h>
int main()
{
    long int a,c,b,ll,n;
    printf("Ievadiet vienu decimāldaļskaitli: ");
    scanf("%ld",&n);
    printf("Izvēlētiet datu tipu(char-c; int-b; long long-ll)\n: ");
    scanf("%ld",&a);
    
    int i,factorial;
    factorial=1;
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
     for(i=1; i<=n; i++)
        {
         factorial = factorial * i;
        }
     printf("Faktoriāls no ievadītā skaitļa (%ld) ir : %d",n,factorial);
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
     for(i=1; n>=13; i++)
        {
         printf("Faktoriāls no ievadītā skaitļa: Faktoriālam nav vērtības\n");
         break;
        }
    }
return 0;
}

    PU6: user defined function

    N1-bez argumentiem un bez return
#include <stdio.h>
void skaitlu_paarbaude();

int main()
{
 skaitlu_paarbaude(); //bez argumentiem
 return 0; //bez return
}
void skaitlu_paarbaude()
{
 int n, i, flag=0;
 printf("Ievadiet pozitīvu veselu skaitli: ");
 scanf("%d",&n);
 for(i=2; i<=n/2; i++)
 {
  if(n%i==0)
  {
   flag=1;
  }
 }
if (flag==1)
 printf(" %d nav pamata skaitlis.", n);
else
 printf(" %d ir pamata skaitlisr.", n);
}

    N2-ar argumentiem un bez return
#include <stdio.h>
void priekshskatiijuma_un_displeja_paarbaude(int n);

int main()
{
 int n;
 printf("Ievadiet pozitīvu veselu skaitli: ");
 scanf("%d",&n);//n-arguments
 priekshskatiijuma_un_displeja_paarbaude(n);
return 0;//bez return
}
void priekshskatiijuma_un_displeja_paarbaude(int n)
{
 int i, flag = 0;
 for(i=2; i<=n/2; ++i)
 {
  if(n%i==0)
  {
   flag=1;
   break;
  }
 }
if(flag == 1)
 printf(" %d nav pamata skaitlis.",n);
else
 printf(" %d ir pamata skaitlis.", n);
}

    N3-bez argumentiem un ar return
#include <stdio.h>
int ieguut_veselu_skaitli();

int main()
{
 int n, i, flag=0; //bez argumentiem
 n = ieguut_veselu_skaitli();
 for(i=2; i<=n/2; ++i)
 {
  if(n%i==0){
  flag = 1;
  break;
 }
}
if (flag == 1)
 printf(" %d nav pamata skaitlis.", n);
else
 printf(" %d ir pamata skaitlis.", n);
return 0;
}//ar return
int ieguut_veselu_skaitli()
{
 int n;
 printf("Ievadiet pozitīvu veselu skaitli: ");
 scanf("%d",&n);
return n;
}

    N4-ar argumentiem un ar return
#include <stdio.h>
int skaitlu_paarbaude(int n);

int main()
{
 int n, flag;
 printf("Ievadiet pozitīvu veselu skaitli: ");
 scanf("%d",&n); //n-arguments un ar return
 flag = skaitlu_paarbaude(n);
 if(flag == 1)
  printf(" %d nav pamata skaitlis",n);
 else
  printf(" %d ir pamata skaitlis",n);
return 0;
}
int skaitlu_paarbaude(int n)
{
 int i;
 for(i=2; i<=n/2; i++)
 {
  if(n%i == 0)
  return 1;
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

                                                07.01.2021-...

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
