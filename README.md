# data
#include <stdio.h>
#include <stdlib.h>
typedef struct node
{
    int data;
    struct node *next;

}node;
node *head;
node *temp;
int count=1;
void insert(int x)
{
    node* newnode=(node*)malloc(sizeof(node));
    newnode->data=x;
    newnode->next=NULL;
    if (head==NULL)
    {
        head=newnode;
        temp=newnode;


    }
    else
    {
        temp->next=newnode;
        temp=newnode;
        count+=1;
    }
}
void pop()
{
    if (head==NULL)
    {
        printf("NOTHING TO POP\n");

    }
    else
    {
        head=head->next;
    }
}
void print()
{
    node* u=head;
    while(u!=NULL)
    {
        printf("%d",u->data);
        u=u->next;
    }
}
int main()
{

    insert(3);
    insert(6);
    print();
}
