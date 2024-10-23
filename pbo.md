import java.util.Scanner;

public class ZakatMallCalculator {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double nisab = 85000000; // Batas minimal harta (85 juta rupiah)
        double harta = 0;

        // Perulangan hingga pengguna memasukkan jumlah harta yang mencapai nisab
        while (true) {
            System.out.printf("Masukkan jumlah harta (uang) dalam bentuk desimal (minimal %.0f): ", nisab);
            harta = scanner.nextDouble();

            // Memeriksa apakah jumlah harta mencapai nisab
            if (harta >= nisab) {
                break;
            } else {
                System.out.println("Jumlah harta belum mencapai nisab, silakan masukkan lagi.");
            }
        }

        // Menghitung zakat sebesar 2.5% dari total harta
        double zakat = harta * 2.5 / 100;

        // Menampilkan jumlah zakat yang harus dibayarkan
        System.out.printf("Jumlah zakat yang harus dibayarkan adalah: %.2f/n" , zakat);
                              scanner.close();
           }
        }
