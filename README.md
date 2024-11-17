# Aplikasi Pertambahan Dua Angka
 Latihan1 -  Muhammad Ihsan - 2210010286

### 1. Deskripsi Program:
   
   • Pengguna memasukkan dua angka

   • Saat tombol Tambah diklik akan menampilkan hasil pertambahan

   • Saat tombol Hapus diklik akan menghapus nilai di TextField dan
   mengarahkan fokus ke TextField angka pertama

### 2. Komponen GUI: JFrame, JPanel, JLabel, JTextField, JButton

### 3. Logika Program: Penambahan dua angka, validasi input numerik

### 4. Events: ActionListener untuk tombol Tambah, Hapus, dan Keluar
   
#### A.Tambah
```
   private void TombolTambahActionPerformed(java.awt.event.ActionEvent evt) {                                             
        try {
        int angka1 = Integer.parseInt(Angka1.getText());
        int angka2 = Integer.parseInt(Angka2.getText());
        int hasil = angka1 + angka2;
        Hasil.setText(" " + hasil);
 ```   


#### B.Hapus
```
  private void TombolHapusActionPerformed(java.awt.event.ActionEvent evt) {                                            
        // TODO add your handling code here:
        Angka1.setText("");
        Angka2.setText("");
        Hasil.setText("");
        Angka1.requestFocus();
    }  
```

#### C.Keluar
 ```
  private void TombolKeluarActionPerformed(java.awt.event.ActionEvent evt) {                                             
        // TODO add your handling code here:
        System.exit(0);
    }                                         
 ```
### 5. Variasi: 
#### A.KeyAdapter pada JTextField untuk membatasi input hanya angka
```
     private void Angka1KeyTyped(java.awt.event.KeyEvent evt) {                                
        // TODO add your handling code here:
        char karakter = evt.getKeyChar();
    if (!Character.isDigit(karakter)) {
        evt.consume(); 
    }
```
####  B.Gunakan JOptionPane untuk menampilkan error input
```
} catch (NumberFormatException e) {
        JOptionPane.showMessageDialog(this, "Masukkan angka yang valid!", "Error", JOptionPane.ERROR_MESSAGE);
    }
```
#### C.Implementasikan FocusListener untuk membersihkan JTextField
saat mendapatkan fokus.
```
    private void Angka1FocusGained(java.awt.event.FocusEvent evt) {                                   
        // TODO add your handling code here:
        Angka1.setText("");
    }
```
## Foto Aplikasi Setelah di Run
![Latihan1](https://github.com/user-attachments/assets/b5403741-6852-45ed-89f8-48aa688f4d7a)

 

## Indikator Penilaian:

| No  | Komponen         |  Persentase  |
| :-: | --------------   |   :-----:    |
|  1  | Komponen GUI     |    20    |
|  2  | Logika Program   |    20    |
|  3  | Kesesuaian UI    |    15    |
|  4  | Constructor      |    15    |
|  5  | Memenuhi Variasi |    30    |
|     | TOTAL        | 100 |

## Pembuat

Nama : Muhammad Ihsan
NPM : 2210010286
