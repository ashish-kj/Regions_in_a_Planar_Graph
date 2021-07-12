import java.util.*;

public class Region 
{
    
    public static int calcRegion(int v,int e)
    {
        int r;
        r = e - v + 2;
        return r;
    }

    public static void main(String[] args) 
    {
        Scanner s = new Scanner(System.in);
        
        int i=0;
        int n;
        
        char arr[] = new char[26];
        for(i=0;i<26;i++)
        {
            arr[i]=(char)(i+65);
        }
        
        System.out.println("Please Enter The Number Of Vertices In The Graph");
        n=s.nextInt();
        System.out.print("Let the vertices be:-");
        for(i=0;i<n;i++)
        {
            if(i<n-1)
            {
                System.out.print(arr[i]+",");
            }
            else
            {
                System.out.println(arr[i]);
            }
        }
        System.out.println("Enter the adjacency list one by one:-");
        i=0;
        String al;
        String[] ale = new String[n];
        int sum=0;
        
        for(i=0;i<n;i++)
        {
            System.out.print("Enter the vertices connected to vertex "+arr[i]+" :");
            if(i==0)
            s.nextLine();
            al=s.nextLine();
            ale = al.split(" ");
            sum = sum + ale.length;
        }
        int e;
        e=sum/2;
        int r;
        r = calcRegion(n,e);
        
        System.out.println("The number of regions in this graph is: "+r+" .");
        
        
    }
    
}
