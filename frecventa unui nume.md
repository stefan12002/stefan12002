import java.text.CollationElementIterator;
import java.util.*;

public class Main {
    public static void main(String[] args) {
/*     //Crearea obiectului din lista(poate fi LinkedList sau ArrayList)
        LinkedList<Integer>listA=new LinkedList<Integer>();
        //adaugare elemente in lista;
        int nr;
        int a=10;
        Scanner in=new Scanner(System.in);
        while(a!=0){
            nr=in.nextInt();
            listA.add(nr);
            a--;
        }
        //stergere elemente impare din lista
        listA.removeIf(n->(n%2!=0));
        for(int i:listA){
            System.out.print(i+" ");
        }*/
LinkedList<String>V=new LinkedList<String>();
        V.add("Ana");
        V.add("Maria");
        V.add("Schwaini");
        V.add("Neuer");
        V.add("Lewandowski");
        V.add("Muller");
        V.add("Lahm");
        V.add("Robben");
        V.add("Neuer");
        V.add("Ribery");
        V.add("Kroos");
        V.add("Lahm");
        V.add("Schwaini");
        V.add("Neuer");
        V.add("Kimmich");
        V.add("Lahm");
        V.add("Boateng");
        V.add("Gnabry");
        Collections.sort(V);
            System.out.println(V);
            Set<String>distinct=new HashSet<>(V);

            for(String i:distinct){
                    System.out.println(i+":"+Collections.frequency(V,i));

            }
            String a=" ";
            int max=-1;
        for(String i:distinct) {
            if (Collections.frequency(V, i) > max) {
                max = Collections.frequency(V, i);
                a = i;
            }
        }
            int min=10000;
            System.out.println("primul nume care apare de cele mai multe ori este: "+a);
            for(String j:distinct) {
                if(Collections.frequency(V,j)<min){
                    min=Collections.frequency(V,j);
                    a=j;
                }
        }
        System.out.println("primul nume care apare de cele mai putine ori este "+ a);

            Collections.reverse(V);
        System.out.println(V);

            }
}
