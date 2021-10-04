# Recursive Bubble Sort using C

Recursive bubble sorting in C is the sorting algorithm used to organize a list in a particular way, which can be ascending or descending in numerical or lexicographic order. It is one of the most used algorithms in C, which includes classification by combination and classification by selection.

[Bubble Sort using recursion](https://www.techgeekbuzz.com/recursive-bubble-sort-in-c/) is the simplest sorting algorithm. It is so named  because the smallest or largest items, depending on whether the order is descending or ascending, are "blown" to the top of the list.

![Recursive Bubble Sort using C](https://secureservercdn.net/160.153.137.163/84g.4be.myftpupload.com/wp-content/uploads/2019/01/Recursive-Bubble-Sort-in-C-665x333.png)

## What is Recursive Bubble Sort?

Recursion refers to repetition  using smaller input values. It does this on the current input by applying simple functions to the returned value. There are several ways to perform bubble classification, including the following: 

* Arrays,
* Pointers,
* Functions, and
* Recursion

When we do recursive bubble classification, it is called recursive bubble classification. The recursive function calls itself until we get the ordered data. The advantages and disadvantages of the recursive bubble type are  the same as those of the bubble type. However, in most cases it is a superior alternative to the simple bladder variety. 

As we know, in  bubble sorting, we use a comparison-based technique to sort a matrix. We first compare the two initial elements to each other and place the smallest in the  first position. Then in the second comparison or second pass, we begin to compare the elements in the second and third position. This continues until the list is sorted.

To understand the recursive bubble sort in C better, we are here to explain an example. Before diving into the code, let’s first understand the algorithm that we will be using here.

**Algorithm**

**STEP 1:** If the array size is 1, then return.
**STEP 2:** Do One Pass of normal Bubble Sort on the given array. This will fix the last element of the current subarray.
**STEP 3:** Use Recursion for all elements except the last of the current subarray.

**Example:**

```
#include<stdio.h>
void BubbleSortRecursion(int a[],int num);
main()
{
int i,j,num,temp;
printf("Enter number of elements\n");
scanf("%d",&num);
int a[num];
printf("Enter numbers\n");
for(i=0;i<num;i++)
{
 scanf("%d",&a[i]);
}
BubbleSortRecursion(a,num);
printf("Given numbers in Ascending order \n");
for(i=0;i<num;i++)
{
 printf("%d\n",a[i]);
}
}
void BubbleSortRecursion(int a[],int num)
{
 int i,j,temp;
 i=num;
if(i>0)
  {
       for(j=0;j<num-1;j++)
       {
         if(a[j]>a[j+1])
          {
            temp=a[j];
            a[j]=a[j+1];
            a[j+1]=temp;
          }
      }
  BubbleSortRecursion(a,num-1);
  }
else
  {
       return;
   }
}
```

**Example Output:**

**Enter the number of elements**

6

**Enter numbers**

75
14
98
13
41
26

**Given numbers in Ascending order**

13
14
26
41
75
98

**Example Using C Programming**

```/* BUBBLE SORT PROGRAM IN C USING RECURSION */
#include <stdio.h>
#include <stdlib.h>
  /* To sort the given numbers in ascending order */
  void bubbleSort(int *data, int n) {
        int i, temp;
        if (n > 0) {
                for (i = 1; i < n; i++) {
                        if (data[i - 1] > data[i]) {
                                temp = data[i];
                                data[i] = data[i - 1];
                                data[i - 1] = temp;
                        }
                }
                bubbleSort(data, n - 1);
        }
        return;
  }
  int main() {
  int i, n, *data;
        /* Enter the numbers of inputs which is to be sorted */
        printf("Enter the number of inputs:");
        scanf("%d", &n);
        /* To store input values, it allocates dynamic memory */
        data = (int *) malloc(sizeof(int) * n);
        /* Enter the input data */
        for (i = 0; i < n; i++) {
                printf("data[%d]: ", i);
                scanf("%d", &data[i]);
        }
        /* sorts the given numbers */
        bubbleSort(data, n);
        /* print the sorted numbers */
        printf("Sorted array:\n");
        for (i = 0; i < n; i++) {
                printf("%d ", data[i]);
        }
        printf("\n");
        return 0;
  }
  ```
  
**Example Output:**

**Enter the number of inputs**

34, 99, 11, 25, 12, 21, 64

**Sorted array:**

11 12 21 25 34 64 99

**Conclusion**

That sums up this demonstration of enforcing a recursive bubble kind in C. Please observe that this isn't always a commonplace manner of enforcing bubble kind the usage of recursion in C.

You can, therefore, write code that does the identical however isn't the same as the only stated above. Do allow us to recognise in case you achieve this thru the feedback segment below. All the best!

