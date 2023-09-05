# Java_Sum
import java.io.*;

/**
 * 𝑎𝑎 + 𝑏𝑏 を 𝑐𝑐 回繰り返すプログラム
 * 2 3 4 と引数を指定すると，
 * 出力は，Sum (ABC) is 20.0 (（2+3)×4)
 */
public class SumWhile{
    public static void main(String[] args){
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // 標準入力
        int a, b, c; 
        String line;
        int sum = 0; // 合計
        int stop = 0; // 回数
        try{
            System.out.print("a = ");
            line = br.readLine();
            a = Integer.parseInt(line); // aの入力値をint型に変更
            System.out.print("b = ");
            line = br.readLine();
            b = Integer.parseInt(line); // bの入力値をint型に変更
            System.out.print("c = ");
            line = br.readLine();
            c = Integer.parseInt(line); // cの入力値をint型に変更
            System.out.println(a + "," + b + "," + c);
            while(stop < c){
                // c回足し算を繰り返す
                sum = sum + a + b;
                stop += 1;
            }
            System.out.println("Sum(ABC) is " + sum); // 結果を出力
        }catch(IOException e){
            System.out.println(e.getMessage());
        }
    }
}
