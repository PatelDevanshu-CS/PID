 #include<stdio.h>
char login();
char main_menu();
char Traffic_logged();
char EMV_signal();
char Traffic_clear();
#define COLOR_BOLD "\e[31m"
#define COLOR_OFF  "\e[m"

char login()
{
    char userid[20],password[20];
    int x,y;
    printf("Enter your userid:");
    scanf("%s",userid);
    printf("Enter your password:");
    scanf("%s",password);
    x=strcmp(userid,"root");
    if(x==0)
    {
        y=strcmp(password,"ggmf1");
        if(y==0)
        {
            printf("Login Successful\n");
            main_menu();
        }
        else
        {
            printf("Invalid Password");
        }
    }
    else
    {
        printf("Invalid Username");
    }
}
char main_menu()
{
    int choice;
    printf("MAIN MENU\n");
    printf("Press 1 for Traffic clear\n");
    printf("Press 2 for EMVs Signal\n");
    printf("Press 0 to Exit\n");
    printf("Enter Your choice:");
    scanf("%d",&choice);
    switch(choice)
    {
        case 1:
        Traffic_logged();
        break;
        case 2:
        EMV_signal();
        break;
        case 0:
        break;
        default:
        printf("Invalid choice");
        break;
    }
}
char Traffic_logged()
{
    int choice1;
    printf(COLOR_BOLD"CHAOSSSSSSSSSS!!!!\n"COLOR_OFF);
    printf("Press 1 to Make Signal RED\n");
    printf("Press 2 to Make Signal YELLOW\n");
    printf("Press 3 to Make Signal GREEN\n");
    printf("Press 4 to go to Main Menu\n");
    printf("Press 0 to Exit\n");
    printf("Enter Your Choice:");
    scanf("%d",&choice1);
    switch(choice1)
    {
        case 1:
        {
         printf("RED\n");
        }
        break;
        case 2:
        {
         printf("YELLOW\n");
        }
        break;
        case 3:
        {
         printf("GREEN\n");
        }
        break;
        case 4:
        main_menu();
        break;
        case 0:
        break;
        default:
        printf("Invalid choice");
        break;
    }
}
char EMV_signal()
{
    char coming[10],stopped[10],Reached[10];
    printf("Input for Coming:");
    scanf("%s\n",coming);
    printf("Input for stop:");
    scanf("%s\n",stopped);
    printf("Input for Reached:");
    scanf("%s\n",Reached);
  
}


int main()
{printf("*********************************************************************************\n");
printf("                      Traffic Clearance for EMVs Using AI\n        ");
printf("                   Developed By:Patel Devanshu\n");
printf("                        Essentials of Software and Programming-1\n");
printf("                                YEAR:2022-2023 \n");
printf("*********************************************************************************\n");
    login();
return 0;
}
