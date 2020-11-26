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
