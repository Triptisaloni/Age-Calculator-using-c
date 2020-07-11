# Age-Calculator-using-c

 #include<stdio.h>
void main()
{
    int a,b,c,x,y,z,day,year,month,feb;
    
    printf("Enter your date of birth(dd/mm/yy) - ");
    scanf("%d/%d/%d",&a,&b,&c);
    printf("Enter current date(dd/mm/yy) - ");
    scanf("%d/%d/%d",&x,&y,&z);
    
    if (z % 400 == 0) 
    feb = 29;
    else if (z % 100 == 0) 
    feb = 28;
    else if (z % 4 == 0) 
    feb = 29;
    else 
    feb = 28;

    
    if(x >= a)
    day = x - a;
    else
    {
        if(y==1||y==3||y==5||y==7||y==8||y==10||y==12)
        day = (x+31)-a;
        else if(y==4||y==6||y==9||y==11)
        day = (x+30)-a;
        else
        day = (x+feb)-a;
        
             y--;
       }
    
    if(y>=b)
    month = y-b;
    else
    {month = (y+12)-b;
    z--;}
    
    year = z-c;
    printf("Age is %d years %d months %d days",year,month,day);
    getch();
}
