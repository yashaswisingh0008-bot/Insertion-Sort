# Insertion-Sort
This is a code for insertion sort

    #include <stdio.h>

    int main() {
    int size;

    printf("Enter number of elements: ");
    scanf("%d", &size);

    int array[size];

    printf("Enter elements:\n");
    for(int i = 0; i < size; i++)
        scanf("%d", &array[i]);

    for(int i = 1; i < size; i++) {
        int currentElement = array[i];
        int j = i - 1;

        while(j >= 0 && array[j] > currentElement) {
            array[j + 1] = array[j];
            j--;
        }

        array[j + 1] = currentElement;
    }

    printf("Sorted array:\n");
    for(int i = 0; i < size; i++)
        printf("%d ", array[i]);

    return 0;
    }
