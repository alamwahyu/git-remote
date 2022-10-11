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

    * **updateListPTEN** >> Merchant yang ingin data Non PTEN nya di update, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Merchant List](https://bni-bmm.spesandbox.com/inputer/merchant)
        3. Filter data berdasarkan merchant yang active
        4. Pilih merchant yang ingin di edit data PTEN 
        5. Pastikan merchant sedang tidak dalam proses lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list)(tidak dalam status  *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN* )
        6. Ganti variabel **updateListPTEN** dengan merchant yang dipilih    

    * **editAggregator** >> Aggregator yang ingin diedit namanya, bisa dipilih menggunakan cara :
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator dengan status Active
        4. Ganti variabel **editAggregator** dengan merchant yang dipilih 
    
    * **noPengajuanDataToRevision** >> Data Add Merchant yang perlu direvisi datanya, bisa dipilih menggunakan cara :
        1. Login sebagai inputer
        2. Masuk ke halaman [Request List - Daftar Tugas Inputer](https://bni-bmm.spesandbox.com/daftar-tugas/inputer-list)
        3. Filter data berdasarkan **jenis pengajuan** *Add New Merchant*
        4. Pilih salah satu merchant, kemudian copy Nomor pengajuannya dan ganti isi variabel **noPengajuanDataToRevision**

    * **subMerchantAggregatorList** >> Aggregator utama yang di gunakan untuk testing modul subMerchant di AggregatorList, Bisa dipilih menggunakan cara: 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator dengan status Active
        4. Pastikan **Aggregator** yang dipilih memiliki data submerchant
        5. Ganti variabel **subMerchantAggregatorList** dengan merchant yang dipilih 

    * **subMerchantAggregatorListEdit** >> Sub merchant yang ingin diedit datanya, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator yang diisi di variable **subMerchantAggregatorList**
        4. Klik tombol titik 3 di bagian paling kanan tabel dan pilih View List Sub Merchant
        5. Filter data berdasarkan status active
        6. Pilih sub merchant dan gantikan variabel **subMerchantAggregatorListEdit** dengan yang dipilih
        7. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)

    * **subMerchantAggregatorListEditnonPTEN** >> Sub merchant yang ingin diedit datanya, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator yang diisi di variable **subMerchantAggregatorList**
        4. Klik tombol titik 3 di bagian paling kanan tabel dan pilih View List Sub Merchant
        5. Filter data berdasarkan status active
        6. Pilih sub merchant dan gantikan variabel **subMerchantAggregatorListEditnonPTEN** dengan yang dipilih
        7. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)

    * **subMerchantAggregatorListClose** >> Sub merchant yang ingin diedit datanya, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator yang diisi di variable **subMerchantAggregatorList**
        4. Klik tombol titik 3 di bagian paling kanan tabel dan pilih View List Sub Merchant
        5. Filter data berdasarkan status active
        6. Pilih sub merchant dan gantikan variabel **subMerchantAggregatorListClose** dengan yang dipilih
        7. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)

    * **subMerchantAggregatorListBulkUploadPTEN** >> Sub merchant yang ingin diedit datanya, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator yang diisi di variable **subMerchantAggregatorList**
        4. Klik tombol titik 3 di bagian paling kanan tabel dan pilih View List Sub Merchant
        5. Klik tombol Bulk Upload Update PTEN
        7. Pilih merchant yang ingin diupdate datanya
        8. Pilih sub merchant dan gantikan variabel **subMerchantAggregatorListBulkUploadPTEN** dengan yang dipilih (Pastikan sub merchant sedang tidak dalam proses Edit)
        9. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)
        10. Kemudian klik download template
        11. Edit file xlsx dengan data yang ingin diupdate
        12. Masukan file tersebut ke dalam folder templateBulk dan rename file nya menjadi *EditBulkSubMerchant_PTEN.xlsx*

    * **subMerchantAggregatorListBulkUploadNonPTEN** >> Sub merchant yang ingin diedit datanya, bisa dipilih menggunakan cara : 
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Aggregator List](https://bni-bmm.spesandbox.com/inputer/aggregator)
        3. Filter data berdasarkan Aggregator yang diisi di variable **subMerchantAggregatorList**
        4. Klik tombol titik 3 di bagian paling kanan tabel dan pilih View List Sub Merchant
        5. Klik tombol Bulk Upload Update Non PTEN
        7. Pilih merchant yang ingin diupdate datanya
        8. Pilih sub merchant dan gantikan variabel **subMerchantAggregatorListBulkUploadNonPTEN** dengan yang dipilih (Pastikan sub merchant sedang tidak dalam proses Edit)
        9. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)
        10. Kemudian klik download template
        11. Edit file xlsx dengan data yang ingin diupdate
        12. Masukan file tersebut ke dalam folder templateBulk dan rename file nya menjadi *EditBulkSubMerchant_NonPTEN.xlsx*
    * **listOutlet** >> Sub merchant yang digunakan untuk testing fitur di menu list outlet, bisa dipilih menggunakan cara :
        1. Login sebagai inputer
        2. Masuk ke halaman [Inputer List - Inputer Sub Merchant](https://bni-bmm.spesandbox.com/inputer/sub-merchant)
        3. Filter data menggunakan status active
        4. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)
        5. Ganti variable **listOutlet** dengan sub merchant yang dipilih.
    * **AggregatorForTestSubmerchant** >> Nama aggregator yang digunakan untuk testing menu sub merchant di aggregator list, bisa dipilih menggunakan cara:
        1. login sebagai admin
        2. Masuk ke halaman [Client List - Aggregator List](https://bni-bmm.spesandbox.com/client/aggregator)
        3. filter data berdasarkan *Nama aggregator* dengan nama *auto* (bisa juga menggunakan nama lain, tapi untuk amannya menggukan merchant auto) dan filter data berdasarkan *Status* *Active*
        4. Pastikan sub merchant sedang tidak dalam proses waiting lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list) (tidak dalam status *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN*)
        5. Ganti variable **AggregatorForTestSubmerchant** dengan Aggregator yang dipilih.
    * **midMerchantToChangeSettlement** >> MID merchant yang akan digunakan untuk dirubah settlementnya, bisa dipilih menggunakan cara :
        1. Login sebagai inputer
        2. Filter data berdasarkan settlement type H+1
        3. Pilih salah satu merchant yang inigun dirubah settlementnya
        4. Pastikan merchant sedang tidak dalam proses lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list)(tidak dalam status  *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN* )
        5. Ganti variable **midMerchantToChangeSettlement** dengan mid merchant yang dipilih
    * **midMerchantToChangeSettlementAll** >> MID merchant yang akan digunakan untuk dirubah settlementnya, bisa dipilih menggunakan cara :
        1. Login sebagai inputer
        2. Filter data berdasarkan settlement type H+1
        3. Pilih salah satu merchant yang inigun dirubah settlementnya
        4. Pastikan merchant sedang tidak dalam proses lewat menu [Inputer Tracking Pengajuan](https://bni-bmm.spesandbox.com/inputer-tracking-pengajuan/list)(tidak dalam status  *Need Revision*, *On progress Approver 1*,*On progress Approver 2*,*Send to PTEN* )
        5. Ganti variable **midMerchantToChangeSettlementAll** dengan mid merchant yang dipilih


2. File Bulk Create
    * Bulk Upload Merchant
        1. File ada di folder = templateBulk/Bulk_upload_Merchant.xlsx 
        ![Lokasi file bulk upload Merchant](https://drive.google.com/uc?export=view&id=1JWHDizdU33X2-FsDpDox30rzZi-LQjWq)
        2. Pastikan data di kolom MID, No Rek BNI, Nama Merchant, Nama Pemilik Usaha, No KTP, No NPWP, Email Pemilik usaha, dan No HP belum terdaftar.
    
    * Bulk Upload Sub Merchant
        1. File ada di folder templateBulk/Bulk_Upload_SubMerchant.xlsx
        2. Pastikan data di kolom MID, No Rek BNI, Nama Merchant, Nama Pemilik Usaha, No KTP, No NPWP, Email Pemilik usaha, dan No HP belum terdaftar.

## **Cara running Script**        
Untuk menjalankan script automation, bisa menggunakan perintah :
- File tertentu : npx codeceptjs run <nama file> contoh *npx codeceptjs run
.\testCase\login.js*
- Menjalankan semua skenario : *npm run test*
- Menjalankan semua skenario beserta reporting menggunakan mochawesome : *npx codeceptjs run --steps --reporter mochawesome*
- Menjalankan skenario MainFlow : *npx codeceptjs run --grep "MainFlow" --reporter mochawesome --steps*
