# simple billing mechine
 #include<stdio.h>
#include<string.h>


struct list
{
    int id;
    char itemName[30];
    int price;
};

        //create function to display bill 
void display(struct list l[] , int size, char cName[] , char cAddres[]){
    int total = 0;
    printf("\n\n\n");
    printf("\t TOUKIR's STORE \n");
    printf("\t---------------- \n");
    printf("\n");
    printf("Name : %s \t Address : %s \n", cName, cAddres);
    printf("\n");
    for (int i = 0; i <size ; i++)
    {
        printf("ID: %d\t", l[i].id);
        printf("Name : %s\t", l[i].itemName);
        printf("ID: %d\n", l[i].price);
        printf("-----------------------------------------------------\n");
        total+=l[i].price;

    }
    printf("\t\tTotal : %d" , total);
    printf("\n\n");
    printf("\t\tThanks for visiting \n");
    printf("\n\n");
    
}

int main(){
    printf("Hello..........\n");
    char Name[30];
    char Address[30];
    int totalItems;
    printf("Enter your name:\t");
    scanf(" %s",&Name);
    printf("Enter your Address:\t");
    scanf(" %s",&Address);
    printf("Enter Total Items:\t");
    scanf("%d",&totalItems);
    printf("\n");


          //struct array 
    struct list l[totalItems];
        //insert items
    for (int i = 0; i < totalItems; i++)
    {
        l[i].id = (i+1);
        printf("Enter %d item name \t" , i+1);
        scanf(" %s", &l[i].itemName);
        printf("Enter price \t");
        scanf("%d" , &l[i].price);
    }
    //call display  function
    display(l , totalItems , Name , Address);
    
}
