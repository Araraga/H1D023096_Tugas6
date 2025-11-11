# Proses Passing Data dari Form Menuju Tampilan

1. Pengambilan Data  
   Pertama, data diambil dari input pengguna. Ini terjadi di dalam event onPressed pada ElevatedButton di file form_data.dart. Data teks diambil dari TextEditingController menggunakan properti .text.  Tahun lahir (_birthYearController.text) dikonversi menjadi int dan dihitung umurnya.

2. Navigasi dan Pengiriman  
   Setelah data siap, proses navigasi ke halaman baru (TampilDataPage) dimulai menggunakan Navigator.push. Saat membuat MaterialPageRoute, sebuah instance baru dari TampilDataPage dibuat. Data yang sudah disiapkan (name, nim, age) dilewatkan sebagai parameter ke dalam constructor TampilDataPage.

3. Penerimaan Data  
   File tampil_data.dart harus disiapkan untuk menerima data tersebut. Ini dilakukan dengan mendefinisikan variabel final di dalam class dan membuat constructor yang mewajibkan (required) parameter tersebut.

4. Penampilan Data  
   Setelah instance TampilDataPage dibuat dan variabelnya (name, nim, age) terisi, method build() akan dieksekusi.  Di dalam build(), variabel-variabel tersebut (yang sekarang sudah berisi data dari form) dapat langsung digunakan untuk ditampilkan di dalam Text widget.


