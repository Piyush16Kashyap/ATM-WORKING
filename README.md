#include<stdio.h>
#include<conio.h>
#include<string.h>
#include<dos.h>
int main(){
    char pwd[5];
    int i,j;
    for(j=0;j<3;j++){
    textcolor(BLUE);
    cprintf("\nPassword is case sensitive , so only use small lettes.\n");
    printf("Enter the password : ");
    for(i=0;i<4;i++){
    pwd[i]=getch();
    printf(" %c",pwd[i]);
   delay(500);
    printf("\b*");
    }
    pwd[i]='\0';
    textcolor(YELLOW);
    cprintf("\n\rPassword Verification Under Process...");
    delay(3000);
    if(strcmp(pwd,"abcd")==0){
    textcolor(GREEN);
    cprintf("\n\rCORRECT PASSWORD");
    break;
    }
    else{
    textcolor(RED);
    cprintf("\n\rINVALID PASSWORD\n");
    }
    printf("TRY AGAIN\n");
    }
    if(j==3){
    textcolor(RED);
    cprintf("\rYOUR CARD IS BLOCK");
    }
    textcolor(ORANGE);
    cprintf("\n\rTHANK YOU FOR USING ME");
    return 0;
}
