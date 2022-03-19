
import java.util.Scanner;
import  java.io.*;
import java.io.FileNotFoundException;
import java.io.File;
import java.util.*;
import java.io.FileWriter;
public class Main {
    public static void main(String[] args) {
        String filePath="D:\\Java citire si scriere\\exercitiul6";
        String filename="Rezultat.txt";
        File fisierObj=new File(filePath+filename);

        int k=1;
        int Size,size1=0,size2=0,size3=0;
        Vector<Integer> v = new Vector<Integer>(1000);
        //Crearea unui fisier
        try{
            if(fisierObj.createNewFile()){
                System.out.println("fisierul a fost creat "+fisierObj.getName());

            }else{
                System.out.println("fisierul exista deja");
            }

        } catch(IOException e){
            System.out.println("Eroare"+e.getMessage());
            e.printStackTrace();
        }
        try{
            File fileObj1=new File("fisier1.txt");
            Scanner fileReader=new Scanner(fileObj1);
            while(fileReader.hasNextLine()){
                String data=fileReader.nextLine();
                int data1=Integer.parseInt(data);
                v.add(data1);
                size1++;
            }
            // fileObj.getAbsolutePath();
            fileReader.close();
        }catch(FileNotFoundException e){
            System.out.println("a aparut o eroare");
            e.printStackTrace();
        }

        try{
            File fileObj2=new File("fisier2.txt");
            Scanner fileReader=new Scanner(fileObj2);
            while(fileReader.hasNextLine()){
                String data=fileReader.nextLine();

                int data1=Integer.parseInt(data);
                    v.add(data1);
                size2++;
            }
            // fileObj.getAbsolutePath();
            fileReader.close();
        }catch(FileNotFoundException e){
            System.out.println("a aparut o eroare");
            e.printStackTrace();
        }
        try{
            File fileObj3=new File("fisier3.txt");
            Scanner fileReader=new Scanner(fileObj3);
            while(fileReader.hasNextLine()){
                String data=fileReader.nextLine();

                int data1=Integer.parseInt(data);
                v.add(data1);
                size3++;
            }
            // fileObj.getAbsolutePath();
            fileReader.close();
        }catch(FileNotFoundException e){
            System.out.println("a aparut o eroare");
            e.printStackTrace();
        }
        Size=size1+size2+size3;
        // System.out.println(size1+" "+size2+" "+size3+" "+Size);

       System.out.println(Collections.max(v)+" "+Size);
        //System.out.println(v+"\n");
        Collections.sort(v);
        for(int i=0;i<Size;i++)
        {
            System.out.println(v.get(i));
        }

        try{  PrintStream out = null;

            out = new PrintStream(new FileOutputStream("Rezultat.txt"));
out.println(Collections.max(v)+" "+Size);
            for (int i = 0; i < Size; i++) {
                out.println( v.elementAt(i));
            }

        }
        catch(IOException e){
            System.out.println("Eroare"+e.getMessage());
            e.printStackTrace();
        }


    }
}
