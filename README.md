//choclate carton distribution
# import java.util.*;

public class Main {


    public static void main(String[] args) {
    
        Scanner sc=new Scanner(System.in);
        int choclate_cartons=sc.nextInt();
        int[] arr=new int[choclate_cartons];
        for(int i=0;i<arr.length;i++){
            arr[i]=sc.nextInt();
        }
        int children=sc.nextInt();
        Arrays.sort(arr);
        int low=0;
        int high=children-1;
        int diff=Integer.MAX_VALUE;
        while(high<arr.length){
            if(arr[high]-arr[low]<diff)
                diff=arr[high]-arr[low];

            low++;
            high++;
        }
        System.out.print(diff);
    }

}
