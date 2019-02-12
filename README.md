# compilerlab
package syntex;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;

public class Syntex {

    public static void main(String[] args) throws FileNotFoundException, IOException {
        File file = new File("C:\\Users\\Israt\\Desktop\\input.txt");
        BufferedReader br = new BufferedReader(new FileReader(file));
        String x;

        System.out.print("Keywords : ");
        while ((x = br.readLine()) != null) {
            String[] y = x.split("[, ;()]");
            int z = x.split(", ;()").length;
            for (int j = 0; j < z; j++) {
                if ("int".equals(y[j]) || "float".equals(y[j]) || "char".equals(y[j]) || "if".equals(y[j]) || "else".equals(y[j])) {
                    System.out.print(y[j] + ",");
                }
            }
        }

        File file1 = new File("C:\\Users\\Arif\\Desktop\\input.txt");
        BufferedReader br1 = new BufferedReader(new FileReader(file1));
        String x1;

        System.out.print("\n" + "Identifires : ");
        while ((x1 = br1.readLine()) != null) {

            String[] y1 = x1.split("[ ]");
            int z1 = x1.split(" ").length;

            for (int j1 = 1; j1 < z1 - 1; j1++) {

                String x11 = ",";
                if ("int".equals(y1[0]) || "float".equals(y1[0]) || "char".equals(y1[0]) || "long".equals(y1[0]) || "double".equals(y1[0])) {
                    x11 += y1[j1];
                }
                String[] y11 = x11.split("[,]");
                int z11 = x11.split(",").length;

                for (int j11 = 1; j11 < z11; j11++) {
                    System.out.print(y11[j11] + ",");

                }
            }
        }
        
        
        
        File file2 = new File("C:\\Users\\Arif\\Desktop\\input.txt");
        BufferedReader br2 = new BufferedReader(new FileReader(file2));
        String x2;

        System.out.print("\n" + "Math Operations : ");
        while ((x2 = br2.readLine()) != null) {
            char ch[]=x2.toCharArray(),ch1[] = null;

            for(int i=0;i<ch.length;i++){
                if(ch[i]=='+'||ch[i]=='-'||ch[i]=='*'||ch[i]=='/'||ch[i]=='='){
                    //ch1[j++]=ch[i];
                    System.out.print(ch[i]+",");
                }
            }
        }
        
        File file3 = new File("C:\\Users\\Arif\\Desktop\\input.txt");
        BufferedReader br3 = new BufferedReader(new FileReader(file3));
        String x3;

        System.out.print("\n" + "Logical Operations : ");
        while ((x3 = br3.readLine()) != null) {

            char ch[]=x3.toCharArray(),ch1[] = null;

            for(int i=0;i<ch.length;i++){
                if(ch[i]=='<'||ch[i]=='>'||ch[i]=='!'||ch[i]=='^'){

                    System.out.print(ch[i]+",");
                }
            }
        }
        
        
        
        
        File file4 = new File("C:\\Users\\Arif\\Desktop\\input.txt");
        BufferedReader br4 = new BufferedReader(new FileReader(file4));
        String x4;

        System.out.print("\n" + "Others : ");
        while ((x4 = br4.readLine()) != null) {

            String a="1234567890";
            char ch[]=x4.toCharArray(),ch1[] = null,ch2[]=a.toCharArray();

            for(int i=0;i<ch.length;i++){
                for(int j=0;j<=9;j++){
                    if(ch[i]==ch2[j]){
                        System.out.print(ch[i]+",");
                    }
                }
            }
        }
        
        
        
        File file5 = new File("C:\\Users\\Arif\\Desktop\\input.txt");
        BufferedReader br5 = new BufferedReader(new FileReader(file5));
        String x5;

        System.out.print("\n" + "Others : ");
        while ((x5 = br5.readLine()) != null) {

            char ch[]=x5.toCharArray(),ch1[] = null;

            for(int i=0;i<ch.length;i++){
                if(ch[i]=='('||ch[i]==')'||ch[i]=='{'||ch[i]=='}'){

                    System.out.print(ch[i]+",");
                }
            }
        }
    }
}
