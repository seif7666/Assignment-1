# Assignment-1
Calculator

public class Main implements ICalculator {
    public static final  int max=Integer.MAX_VALUE;
    public static final  int min=Integer.MIN_VALUE;
    @Override
    public int add(int x, int y) {
        long sum=(long)x+y;
        if(sum<=max&&sum>=min)
        return x + y;
        System.out.println("The sum is not an int");
        return -1;
    }

    @Override
    public float divide(int x, int y) {
        try {
            float z=x/y;
            return (float) x /(float) y;
        } catch (ArithmeticException e) {
            System.out.println(e.toString() + "\nDivision by zero is not allowed.");
            return -1;
        }

    }
}
interface ICalculator{
    public int add(int x,int y);
    public float divide(int x,int y)throws RuntimeException;
}
