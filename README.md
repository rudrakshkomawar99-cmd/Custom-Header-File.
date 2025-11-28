# Custom-Header-File.
This a custom header file in C in VS code . This header file is about some operations of maths  like checking if a no. is prime , even or odd , printing fibonacci series , addition-substraction of matrix 
VSM.h 
#include <stdio.h>


void check_prime(int n) {
   int count =0;
 
    if (n <= 1) {
        printf("%d is not a prime number.\n", n);
    } else {
        for (int i = 2; i <= n; i++) {
            if (n % i == 0) {
                count++;
            }
        }


        if (count == 1) {
            printf("%d is a prime number.\n", n);
         } else {
            printf("%d is not a prime number.\n", n);
         }
    }


   
}


void check_even_odd (int n) {


      if (n == 0) {
          printf("The no. is zero \n");
      }
     
      if(n % 2 == 0) {
        printf("The no. is EVEN \n");
      } else {
        printf("The no. is odd \n");    
      }


}


void print_fib(int a,int b,int n) {
     


     if (n == 0) {
        return;
       
    }
     int c = a + b;
     printf("%d ", c);
     print_fib(b,c,n-1);
}


matrix.h 
#include <stdio.h>




// Function to take 2 matrices and print their addition
void m_add(int n, int m) {
    int arr[n][m];
    int arr1[n][m];
    int sum[n][m];


    printf("Enter elements of Matrix 1:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            scanf("%d", &arr[i][j]);
        }
    }


    printf("Enter elements of Matrix 2:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            scanf("%d", &arr1[i][j]);
        }
    }


    // Adding matrices
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            sum[i][j] = arr[i][j] + arr1[i][j];
        }
    }


    // Printing result
    printf("Addition of both matrices:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            printf("%d ", sum[i][j]);
        }
        printf("\n");
    }
}




// Function to take 2 matrices and print their addition
void m_sub(int n, int m) {
    int arr[n][m];
    int arr1[n][m];
    int sub[n][m];


    printf("Enter elements of Matrix 1:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            scanf("%d", &arr[i][j]);
        }
    }


    printf("Enter elements of Matrix 2:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            scanf("%d", &arr1[i][j]);
        }
    }


    // Adding matrices
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            sub[i][j] = arr[i][j] - arr1[i][j];
        }
    }


    // Printing result
    printf("Substraction of both matrices:\n");
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            printf("%d ", sub[i][j]);
        }
        printf("\n");
    }
}


main.c 
#include <stdio.h>
//Custom Header File
#include "matrix.h"
#include "VSM.h"




int main () {

    
    printf("Functions in custom file : \n ");
    printf("1. Check the no. is even or odd [check_even_odd(no.)]");
    printf("2. Check the no. is prime [check_prime(no.)]");
    printf("3. Print Fibonacci series [print_fib(no.)]");
    printf("4. Print Addition of matrix [m_add(rows,column)]");
    printf("4. Print Substraction of matrix [m_sub(rows,column)]");
    check_even_odd(5);
    check_prime(3);
    print_fib(0,1,5);
    m_add(2,2);
    m_sub(2,2);
   
   
return 0;
}
