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
   * **forgotPassword** >> Akun User yang ingin dilakukan proses forgot password dan password baru nya dapat di tentukan pada data ini, bisa dipakai menggunakan cara :
        1. Login sebagai Admin
        2. Masuk ke halaman [Access Control -> Users](https://apdev.bni-ecollection.com/access-control/user/index)
        3. Filter data Username berdasarkan value **"forgotpassword"**
           - Pastikan Username tersebut sudah terdaftar di portal
           - **Notes** : Jika belum terdaftar, silahkan buat users dahulu dengan Username : **"forgotpassword"**
        4. Ganti variabel **forgotPassword** dengan password yang baru dengan **ketentuan** 
           - Pastikan data env forgotPassword diubah, setiap menjalankan Skenario **[02-01]ForgotPassword**

    * **MIDTesting** >> Memastikan data Merchant ID yang dipilih memiliki List Customer Data dan List Users yang terdaftar, bisa dipilih menggunakan cara :
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter data Status berdasarkan merchant yang active
        4. Pilih merchant ID yang ingin digunakan dengan **ketentuan**   
           - Pastikan merchant yang dipilih adalah merchant yang tidak terpakai lagi atau bisa juga pilih merchant yang mengandung kata automation)
           - Pastikan MID yang dipilih terdapat List Customer Data (VA Number)
           - Pastikan MID terdapat List Akun Users yang terdaftar
        4. Ganti variabel **MIDTesting** dengan merchant yang dipilih

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
        6. Ganti variabel **userDataEdit** dengan users yang dipilih
 
     * **userDataDelete** >> Users yang ingin data akses nya didelete, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by Merchant ID berdasarkan merchant yang telah dipilih yaitu variabel **MIDTesting**
        4. Klik & Masuk ke halaman [Users Data](https://apdev.bni-ecollection.com/merchant/user?id=2) 
        5. Pilih User yang ingin didelete dengan **ketentuan**   
           - Pastikan Users yang dipilih sesuai dan terdaftar
           - Pastikan data user yang dipilih dapat didelete
        6. Ganti variabel **userDataDelete** dengan users yang dipilih

     * **merchantIDForApprove** >> Merchant ID yang ingin data BNI Giro Account nya diubah dan diapprove, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by BNI Giro Status berdasarkan status ACTIVE
        5. Pilih Merchant ID yang ingin diubah account numbernya dengan **ketentuan**   
           - Pastikan Merchant ID tidak sedang menunggu APPROVAL, dapat dicek melalui halaman [Approval Management](https://apdev.bni-ecollection.com/bni/approval/index)
           - Pastikan AccountNumber MID berstatus ACTIVE dan dapat diubah
        6. Ganti variabel **merchantIDForApprove** dengan merchant yang dipilih
        
     * **merchantIDForReject** >> Merchant ID yang ingin data BNI Giro Account nya diubah dan direject, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Merchant Management](https://apdev.bni-ecollection.com/merchant/index)
        3. Filter by BNI Giro Status berdasarkan status ACTIVE
        4. Pilih Merchant ID yang ingin diubah account numbernya dengan **ketentuan**   
           - Pastikan Merchant ID tidak sedang menunggu APPROVAL, dapat dicek melalui halaman [Approval Management](https://apdev.bni-ecollection.com/bni/approval/index)
           - Pastikan AccountNumber MID berstatus ACTIVE dan dapat diubah
        5. Ganti variabel **merchantIDForReject** dengan merchant yang dipilih
        
     * **accNumBillerBilling** >> Account Number Biller Billing yang dibutuhkan untuk proses view & inactive account, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Biller Management -> Biller Billing](https://apdev.bni-ecollection.com/biller-billing/index)
        3. Filter by Account Number berdasarkan biller yang sesuai
        5. Pilih Account Number yang ingin dipakai dengan **ketentuan**   
           - Pastikan terdapat VA pada account numbernya ketika view biller
           - Pastikan account number masih berstatus **ACTIVE**
           - Pastikan terdapat Billing ID yang bisa dilakukan **FORCE DEBIT**
        6. Ganti variabel **accNumBillerBilling** dengan account number yang dipilih

     * **billingIDForceDebit** >> billing ID yang dibutuhkan untuk proses force debit, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Biller Management -> Biller Billing](https://apdev.bni-ecollection.com/biller-billing/index)
        3. Filter by Account Number berdasarkan data yang telah dipilih yaitu variabel **accNumBillerBilling**
        4. Masuk ke halaman [View Biller](https://apdev.bni-ecollection.com/biller-billing/view?id=1741)
        5. Pilih Billing ID yang ingin dipakai dengan **ketentuan**  
           - Pastikan terdapat Billing ID yang dapat dilakukan **FORCE DEBIT**
           - Pastikan Current Balance nya ada
        6. Ganti variabel **billingIDForceDebit** dengan billing ID yang dipilih

     * **accNumBillerAllInactive** >> Account Number yang dibutuhkan untuk proses inactive account, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Biller Management -> Biller All](https://apdev.bni-ecollection.com/biller/index)
        3. Filter by Account Number berdasarkan data yang sesuai
        5. Pilih Account Number yang ingin dipakai dengan **ketentuan**  
           - Pastikan account number berstatus ACTIVE
           - Pastikan terdapat List VA pada account numbernya ketika view biller
        6. Ganti variabel **accNumBillerAllInactive** dengan billing ID yang dipilih

     * **accNumBillerAllforInactiveVA** >> Account Number yang dibutuhkan untuk proses inactive pada VA, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [Biller Management -> Biller All](https://apdev.bni-ecollection.com/biller/index)
        3. Filter by Account Number berdasarkan data yang sesuai
        4. Masuk ke halaman [View Biller Detail -List VA](https://apdev.bni-ecollection.com/biller/view?id=15)
        5. Pilih Account Number yang ingin dipakai dengan **ketentuan**  
           - Pastikan account number berstatus **ACTIVE**
           - Pastikan **LIST VA** pada baris 1 berstatus **ACTIVE**
        6. Ganti variabel **accNumBillerAllforInactiveVA** dengan account NUmber yang dipilih

     * **customerIDFilter | phoneNumberFilter | accountNumberFilter | processTimeFilter | dateFilter** >> Memastikan filter header Merchant Log, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [System Log -> Merchant Log](https://apdev.bni-ecollection.com/system-log/merchant-log)
        3. Pilih data yang sesuai dan lakukan Filter by : *berdasarkan data env diatas*
           - Filter by Customer ID --> ganti variabel **customerIDFilter** dengan data yang dipilih
           - Filter by Phone Number --> ganti variabel **phoneNumberFilter** dengan data yang dipilih
           - Filter by Account Number --> ganti variabel **accountNumberFilter** dengan data yang dipilih
           - Filter by Process Time --> ganti variabel **processTimeFilter** dengan data yang dipilih
           - Filter by Date --> ganti variabel **dateFilter** dengan data yang dipilih

     * **VANumberFilter | dateFilter** >> Memastikan filter header BNI Server Log, bisa dipilih menggunakan cara : 
        1. Login sebagai Admin
        2. Masuk ke halaman [System Log -> BNI Server Log](https://apdev.bni-ecollection.com/system-log/bni-server-log)
        3. Pilih data yang sesuai dan lakukan Filter by : *berdasarkan data env diatas*
           - Filter by VA Number --> ganti variabel **VANumberFilter** dengan data yang dipilih
           - Filter by Date --> ganti variabel **dateFilter** dengan data yang dipilih

## **Cara running Script**        
Untuk menjalankan script automation, bisa menggunakan perintah :
- File tertentu : npx codeceptjs run <nama file> contoh *npx codeceptjs run
.\testCase\login.js*
- Menjalankan semua skenario : *npm run test*
- Menjalankan semua skenario beserta reporting menggunakan mochawesome : *npx codeceptjs run --steps --reporter mochawesome*
- Menjalankan skenario MainFlow : *npx codeceptjs run --grep "MainFlow" --reporter mochawesome --steps*
