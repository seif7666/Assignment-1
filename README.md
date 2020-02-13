# Assignment-1
Calculator

public class Main implements ICalculator {

    @Override
    public int add(int x, int y) {
        return x + y;
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
