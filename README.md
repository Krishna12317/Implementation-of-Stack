# Implementation-of-Stack
Implementation of stack with conditions overflow and underflow
import java.util.Random;
import java.util.Scanner;


class stack
{
    int max;
    int st[];
    int top=-1;
    
    void push(int item)
    {
      if(top==max-1)
            System.out.println("Overflow");
      else
      {
              
            st[++top]=item;
            System.out.println(item+" PUSHED ");
          
      }
    }
    void pop()
    {
        if(top==-1)
            System.out.println("Underflow");
    
    else
        {
    
        System.out.println("The "+st[top--]+" Has Been POPED");
        }
    
    }
   void stack_size(int k)
    {
       max=k;
       st=new int[k];
      
       //top=-1;
    }
    void display()
    {
        if(top==-1)
            System.out.println("STACK IS EMPTY ");
    else
        {
            System.out.print("Elements are :");
          for(int i=top;i>=0;i--)
              
              System.out.print(st[i]+"\t"); 
          
        }

    }
    
}

public class A 
{

     static int p;  
    public static void main(String[] args) 
    {
     
     Scanner sc=new Scanner(System.in) ;  
     Random r=new Random();
     stack1 obj=new stack1();
int ch;
           for(;;)   
           {
        System.out.println("\n1.size of stack1\n2.push\n3.pop\n4.display\n5.exit\n");
        System.out.print("Enter ur choice:");
        ch=sc.nextInt();
        
               
        switch(ch)
        {
            case 1:
                    System.out.println("Enter size of the stack");
                  p=sc.nextInt();
                  obj.stack_size(p);
                  break;
            
            case 2:int RN=r.nextInt(50);
                   obj.push(RN);
                   break;
            case 3:obj.pop();
                 break;
            case 4:obj.display();
                  break;
            case 5:
                 System.exit(0);
            default:System.out.println("\nENTER THE VALID CHOICE");
             
        }
        }
    }
}  
