// Kelas Induk (Parent Class): MasakanSunda
class MasakanSunda {
    private final String bahanUtama;
    private final String caraMembuat;

    public MasakanSunda(String bahanUtama, String caraMembuat) {
        this.bahanUtama = bahanUtama;
        this.caraMembuat = caraMembuat;
    }

    public void infoResep() {
        System.out.println("Resep Masakan Sunda:");
        System.out.println("Bahan Utama: " + bahanUtama);
        System.out.println("Cara Membuat: " + caraMembuat);
    }
}

// Kelas Turunan (Child Class 1): MieKocokBandung
class MieKocokBandung extends MasakanSunda {
    private final String bahanTambahan;

    public MieKocokBandung(String bahanUtama, String caraMembuat, String bahanTambahan) {
        super(bahanUtama, caraMembuat);
        this.bahanTambahan = bahanTambahan;
    }

    public void tambahkanBahanTambahan() {
        System.out.println("Tambahkan bahan tambahan: " + bahanTambahan);
    }
}

// Kelas Turunan (Child Class 2): Lotek
class Lotek extends MasakanSunda {
    private final String bahanTambahan;

    public Lotek(String bahanUtama, String caraMembuat, String bahanTambahan) {
        super(bahanUtama, caraMembuat);
        this.bahanTambahan = bahanTambahan;
    }

    public void tambahkanBahanTambahan() {
        System.out.println("Tambahkan bahan tambahan: " + bahanTambahan);
    }
}

// Kelas Turunan (Child Class 3): SateMaranggi
class SateMaranggi extends MasakanSunda {
    private String bahanTambahan;

    public SateMaranggi(String bahanUtama, String caraMembuat, String bahanTambahan) {
        super(bahanUtama, caraMembuat);
        this.bahanTambahan = bahanTambahan;
    }

    public void tambahkanBahanTambahan() {
        System.out.println("Tambahkan bahan tambahan: " + bahanTambahan);
    }
}

// Program Utama
public class Main {
    public static void main(String[] args) {
        // Membuat objek masakan Mie Kocok Bandung
        MieKocokBandung mieKocok = new MieKocokBandung("Mie jenis lebar", "Rebus mie dan taoge, tumis bumbu halus, sajikan dengan kaldu dan daging.", "Irisan bawang goreng, kucai, kerupuk merah");

        // Membuat objek masakan Lotek
        Lotek lotek = new Lotek("Kangkung, kol, labu siam, kacang panjang, nangka muda, taoge, kentang rebus", "Rebus sayuran hingga matang, sajikan dengan kuah bumbu halus.", "Kerupuk merah");

        // Membuat objek masakan Sate Maranggi
        SateMaranggi sateMaranggi = new SateMaranggi("Daging sapi, lemak sapi", "Marinasi daging dengan bumbu halus, tusuk sate, bakar di atas bara api.", "Irisan cabai dan tomat");

        // Menampilkan informasi resep masing-masing masakan
        mieKocok.infoResep();
        mieKocok.tambahkanBahanTambahan();

        System.out.println();

        lotek.infoResep();
        lotek.tambahkanBahanTambahan();

        System.out.println();

        sateMaranggi.infoResep();
        sateMaranggi.tambahkanBahanTambahan();
    }
}
