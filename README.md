# Stack.c
#include<stdio.h>

#include<stdlib.h>

#define Size 4

int Top=-1, inp_array[Size];
void Push();
void Pop();
void show();

int main()
{
    int choice;

    while(1)
    {
        printf("------------------------------------------------");
        printf("\nOperations performed by Stack\n");
        printf("\n1.Push the element\n2.Pop the element\n3.Show\n4.End\n");
        printf("------------------------------------------------");
        printf("\n\nEnter your choice: ");
        scanf("%d",&choice);

        switch(choice)
        {
            case 1:
                Push();
                break;
            case 2:
                Pop();
                break;
            case 3:
                 show();
                 break;
            case 4:
                exit(0);

            default:
                printf("\nInvalid choice!!\n\n");
                printf("\nPress any key to continue...");
                getch();
                system("cls");
        }
    }
}
void Push()
{
    int x;

    if(Top==Size-1)
    {
        printf("\nOverflow!!");
    }
    else
    {
        printf("\nEnter element to be inserted to the stack: ");
        scanf("%d",&x);
        printf("Element Inserted\n\n");
        Top=Top+1;
        inp_array[Top]=x;
    }
        printf("\nPress any key to continue...");
    getch();
    system("cls");
}

void Pop()
{
    if(Top==-1)
    {
        printf("\nUnderflow!!");
    }
    else
    {
        printf("\nPopped element: %d",inp_array[Top]);
        Top=Top-1;
    }
    printf("\nPress any key to continue...");
    getch();
    system("cls");
}

void show()
{


    if(Top==-1)
    {
        printf("\nUnderflow!!");
    }
    else
    {
        printf("\nElements present in the stack\n\n");
        for(int i=Top;i>=0;--i)
            printf("%d\n",inp_array[i]);
    }
        printf("\nPress any key to continue...");
    getch();
    system("cls");
}
