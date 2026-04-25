# FILES
#include <stdio.h>
int main(){
    FILE *fp;
    int rno;
    char name[20];
    float marks;
    printf("25331A05E8\n");
    fp=fopen("student.txt","w");
    if(fp==NULL){
        printf("The file is cannot open");
    }
    printf("enter the rno,name and marks\n");
    scanf("%d%s%f",&rno,name,&marks);
    fprintf(fp,"%d %s %f",rno,name,marks);
   
    fclose(fp);
    fp=fopen("student.txt","r");
    if(fp==NULL){
        printf("The file is cannot open");
    }
    fscanf(fp,"%d  %s  %f\n",&rno,name,&marks);
    printf(" roll no:%d\n name:%s\n marks: %2.f",rno,name,marks);
    fclose(fp);
    return 0;
}
