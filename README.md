/*   -   -  */
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
struct node
{
    int info;
    struct node *link;

};
struct node *head=NULL;
struct node *temp=NULL;
struct node* createnode()
{
    struct node *n;
    n=(struct node *)malloc(sizeof(struct node));
    return(n);

};
void insertnode()
{
    struct node *t;
    temp=createnode();
    printf("enter a number \n");
    scanf("%d",&temp->info);
    temp->link=NULL ;
    if(head==NULL)
        head=temp;
    else
    {
        t=head;
        while(t->link!=NULL)
             {
             t=t->link;
            t->link=temp;

             }
    }
}
void display()
{
    printf("enterd value is %d\t",temp->info);
    return 0;
}
int main()
{
   int A;
insertnode();
display();
printf("insert again value select 1 \n");
scanf("%d",&A);
switch(A)
{
case'1':
    insertnode();
    display();
    break;
default:
    printf("enter valied code\n");
}
return(0);
getch();
}

