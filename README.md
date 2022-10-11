# AUTOPAY-Portal

## **Step-step installation**
1. Copy URL repository di gitlab dengan cara masuk ke folder projek - klik tombol clone kemudian copy url yang ada di bagian clone with HTTP <br />
![Clone url](https://drive.google.com/uc?export=view&id=1YfB5ugF91K4oYa1aKn4sZIpFx8IixbXG)
2. Buka VS Code, kemudian Klik File - New Windows
3. Kemudian klik tab Source Control atau tekan Ctrl + Shift + G <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1ct4QwDTFFeDFu4hyjLxrIFY8tVGw9A31)
4. Klik tombol Clone Repository, kemudian masukan url repository dan tekan Enter <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1OWyLTVcrVa3mA90w9C5XL-X58M94OcLm)
5. Pilih lokasi penyimpanan file kemudian tunggu sampai proses clone selesai <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=12hsR1rVGqcIgltt-6b4DOBy8KV9wj_sI)
6. Kemudian klik Open saat proses clone selesai
<br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1wfLhV8Jdxff8BaZch7tbA5KJEGU89Xn1)

7. Proses clone sudah selesai <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1c2eAKZRzyEzqOFfm12BCokmsYnKydrS2)
8. Buka terminal dengan cara klik Terminal - New Terminal / Ctrl + Shift + ‘ <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1fXcCy7HnA3CgfeQMSsBrLVXy-BI9Dn6r)
9. Ketikkan “npm install” dan tekan Enter kemudian tunggu sampai proses installasi selesai <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1Q_CrJx5UH1qC4gvxx-0LQg3oD33WZACC)
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1afENtZBp9NADdRSChT_lUxt_qcLl4_LJ)

10. Konfigurasi username, merchant atau data-data yang ingin digunakan untuk testing pada file .env <br />
![Clone vscode 1](https://drive.google.com/uc?export=view&id=1IPml9PQIPEUI4j_9tK_Qv3z-TlpUZajp)
## **Data yang perlu dirubah Sebelum running script**

1. Data di file .env
    * **MIDTesting** >> Memastikan data Merchant ID yang dipilih memiliki List Customer Data dan List Users yang terdaftar, bisa dipilih menggunakan cara :
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter data Status berdasarkan merchant yang active
        4. Pilih merchant ID yang ingin digunakan dengan **ketentuan**   
           - Pastikan merchant yang dipilih adalah merchant yang tidak terpakai lagi atau bisa juga pilih merchant yang mengandung kata automation)
           - Pastikan MID yang dipilih terdapat List Customer Data (VA Number)
           - Pastikan MID terdapat List Akun Users yang terdaftar
        7. Ganti variabel **MIDTesting** dengan merchant yang dipilih

    * **MIDNonRetail** >> Merchant Non Retail yang ingin data merchant nya di update, bisa dipilih menggunakan cara :
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Pilih merchant ID yang ingin diedit dengan **ketentuan**   
           - Pastikan merchant yang dipilih adalah merchant yang tidak terpakai lagi atau bisa juga pilih merchant yang mengandung kata automation)
           - Pastikan Merchant ID bertipe **NON RETAIL**
        4. Ganti variabel **MIDNonRetail** dengan merchant yang dipilih
    * **MIDBilling** >> Merchant Billing yang ingin data merchant nya di update, bisa dipilih menggunakan cara :
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Pilih merchant ID yang ingin diedit dengan **ketentuan**   
           - Pastikan merchant yang dipilih adalah merchant yang tidak terpakai lagi atau bisa juga pilih merchant yang mengandung kata automation)
           - Pastikan Merchant ID bertipe **BILLING**
        4. Ganti variabel **MIDBilling** dengan merchant yang dipilih
        
    * **VAcustomerDataEdit** >> Customer Data yang ingin data VA nya diupdate, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by Merchant ID berdasarkan merchant yang telah dipilih yaitu variabel **MIDTesting**
        4. Klik & Masuk ke halaman [Customer Data](https://apdev.bni-ecollection.com/merchant/biller?id=2) 
        5. Pilih VA yang ingin diedit dengan **ketentuan**   
           - Pastikan VA yang dipilih sesuai dan terdaftar pada CustomerData
        6. Ganti variabel **VAcustomerDataEdit** dengan VA yang dipilih

    * **userDataEdit** >> Users yang ingin data akses nya diupdate, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by Merchant ID berdasarkan merchant yang telah dipilih yaitu variabel **MIDTesting**
        4. Klik & Masuk ke halaman [Users Data](https://apdev.bni-ecollection.com/merchant/user?id=2) 
        5. Pilih User yang ingin diedit dengan **ketentuan**   
           - Pastikan Users yang dipilih sesuai dan terdaftar
           - Pastikan data user yang dipilih dapat diedit
        6. Ganti variabel **userDataEdit** dengan VA yang dipilih
 
     * **userDataDelete** >> Users yang ingin data akses nya didelete, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by Merchant ID berdasarkan merchant yang telah dipilih yaitu variabel **MIDTesting**
        4. Klik & Masuk ke halaman [Users Data](https://apdev.bni-ecollection.com/merchant/user?id=2) 
        5. Pilih User yang ingin didelete dengan **ketentuan**   
           - Pastikan Users yang dipilih sesuai dan terdaftar
           - Pastikan data user yang dipilih dapat didelete
        6. Ganti variabel **userDataDelete** dengan VA yang dipilih

     * **merchantIDForApprove** >> Merchant ID yang ingin data BNI Giro Account nya diubah dan diaktifkan, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by BNI Giro Status berdasarkan status ACTIVE
        5. Pilih Merchant ID yang ingin diubah account numbernya dengan **ketentuan**   
           - Pastikan Merchant ID tidak sedang menunggu APPROVAL
           - Pastikan AccountNumber MID berstatus ACTIVE dan dapat diubah
        6. Ganti variabel **merchantIDForApprove** dengan VA yang dipilih

## **Cara running Script**        
Untuk menjalankan script automation, bisa menggunakan perintah :
- File tertentu : npx codeceptjs run <nama file> contoh *npx codeceptjs run
.\testCase\login.js*
- Menjalankan semua skenario : *npm run test*
- Menjalankan semua skenario beserta reporting menggunakan mochawesome : *npx codeceptjs run --steps --reporter mochawesome*
- Menjalankan skenario MainFlow : *npx codeceptjs run --grep "MainFlow" --reporter mochawesome --steps*
