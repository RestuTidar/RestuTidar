import java.util.ArrayList;

public class Motd5 {
    public static void main(String[] args) {
        ArrayList<Integer> intList = new ArrayList<>();
        intList.add(1);
        intList.add(2);
        intList.add(3);

        ArrayList<Double> doubleList = new ArrayList<>();
        doubleList.add(1.5);
        doubleList.add(2.5);
        doubleList.add(3.5);

        double sumInt = sumOfList(intList);
        double sumDouble = sumOfList(doubleList);

        System.out.println("Sum of Integer list: " + sumInt);
        System.out.println("Sum of Double list: " + sumDouble);
    }

    public static double sumOfList(ArrayList<? extends Number> arrayList) {
        double sum = 0.0;
        for (Number n : arrayList)
            sum += n.doubleValue();
        return sum;
    }
}
