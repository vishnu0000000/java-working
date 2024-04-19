# java matrix
import org.apache.commons.math3.linear.*;

public class MatrixExample {
    public static void main(String[] args) {
        // Define matrices
        RealMatrix matrix1 = MatrixUtils.createRealMatrix(new double[][]{{1, 2, 3}, {4, 5, 6}});
        RealMatrix matrix2 = MatrixUtils.createRealMatrix(new double[][]{{7, 8}, {9, 10}, {11, 12}});

        // Addition
        RealMatrix additionResult = matrix1.add(matrix2);
        System.out.println("Addition Result:");
        printMatrix(additionResult);

        // Multiplication
        RealMatrix multiplicationResult = matrix1.multiply(matrix2);
        System.out.println("Multiplication Result:");
        printMatrix(multiplicationResult);

        // Transposition
        RealMatrix transposeResult = matrix1.transpose();
        System.out.println("Transpose Result:");
        printMatrix(transposeResult);
    }

    // Helper method to print matrices
    public static void printMatrix(RealMatrix matrix) {
        int rows = matrix.getRowDimension();
        int cols = matrix.getColumnDimension();

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                System.out.print(matrix.getEntry(i, j) + " ");
            }
            System.out.println();
        }
        System.out.println();
    }
}

