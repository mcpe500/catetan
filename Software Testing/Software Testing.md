# Pertemuan 1, Introduction to Software Testing

## Introduction to Software Testing
- Software testing dapat diartikan sebagai suatu aktivitas untuk melakukan uji coba software supaya dapat digunakan oleh *end user* atau pengguna. Testing bisa membuktikan adanya *error* tapi tidak bisa membuktikan tiadanya *error*, hal ini disebabkan karena software itu sifatnya terus berkembang.
- Siklus dari SDLC (Software Development Life Cycle):
  1. Planning (Tahap Perencanaan)
	2. Analysis
	3. Design
	4. Implementation
	5. Testing & Integration
	6. Maintenance
- Ada juga dikenal sebagai STLC (Software Testing Life Cycle):
	 1. Requirement Analysis
	 2. Test Planning
	 3. Test Case Development
	 4. Test Environment Setup
	 5. Test Execution
	 6. Test Closure
- *Computer Bug* adalah sebuah kesalahan yang dapat terjadi dalam komputer, hal ini pertama kali disebutkan pada tahun 1947 di *Harvard University* saat sebuah komputer bernama *IBM Mark II* mengalami suatu malfungsi saat menjalankan program, ketika diperiksa ternyata di dalam komputer tersebut terdapat seekor ngengat (*Moth*/*Bug*) sehingga tersebutkan istilah *Bug* untuk mendeskripsikan sebuah program yang terjadi error.
## Sources of Problems
- Requirements Definition - Erroneous, incomplete, inconsisten requirements.
	- Hal ini umumnya diperlukan seorang *System Analyst* yang dimana tugasnya adalah untuk menganalisa sistemnya dan apa yang perlu dilakukan saat suatu kesalahan terjadi.
	- Umumnya *Bug* atau kesalahan harus ditemukan pada saat tahap ini, karena jika tidak ditemukan di tahap ini maka dapat menimbulkan kemunduran dalam *progress* pekerjaan ataupun menyebabkan kerugian finansial.
- Design - Fundamental design flaws in the software.
- Implementation - Careless coding, malicious code.
- Support Systems - Poor programming languages, faulty compilters, misleading development tools.
- Testing - Incomplete testing, poor verification, debugging mistakes.
	- Testing tidak boleh dilakukan hanya dengan 1 metode, dan sebaiknya dilakukan metode yang berbeda-beda.
- Evolution - sloppy redevelopment
## Origin of Bugs
- Umumnya asal-usul dari *bug* adalah:
	- Specifications - 55%
	- Design - 25%
	- Code - 15%
	- Other - 5%
## Spectacular Software Failures
### THERAC-25 Radiation Therapy
- THERAC-25 adalah sebuah mesin terapi radiasi yang dikendalikan oleh komputer mengalami *bug* yang menyebabkan kematian, setidaknya terdapat 6 *malfunction* dari 1985 - 1987.
- Hal ini terjadi karena terjadi *Race condition*.
### Shooting down of Airbus 300
- USS Vincennes menembak sebuah pesawat komersil Airbus 300 pada tahun 1988, hal ini terjadi karena komputer pada USS Vincennes salah mengidentifikasi pesawat Airbus 300 sebagai pesawat *fighter* F-14. Hal ini menyebabkan kematian 290 jiwa.
- Hal ini terjadi karena output yang tidak jelas dan membingungkan dari software-nya.
### The Ariane 5 Disaster
- Pada tahun 1996, sebuah roket luar angkasa bernama Ariane 5 gagal karena 38 detik setelah peluncuran, roket tersebut meledak.
- Hal ini terjadi karena programnya mencoba mengkonversi float 64 bit menjadi *signed integer* 16 bit, menyebabkan *integer overflow*
### Mars Climate Orbiter
- Pada 1998, sebuah *probe* luar angkasa yang seharusnya meneruskan signal dari *Mars Polar Lander* malah menabrakkan diri ke planetnya daripada mendaratkan di orbit dengan selamat.
- Hal ini terjadi karena *bug* gagal mengkonversikan *Imperial system* ke *Metric system*.
## Software Testing Terminologies
- Verification vs Validation
	- Verifikasi berarti "Apakah kita membuat produk ini dengan tepat?"
		- Produk yang dibuat seharusnya sesuai dengan spesifikasi.
	- Sementara validasi berarti "Apakah kita membuat produk yang tepat?"
		- Produk yang dibuat seharusnya sesuai dengan apa yang diinginkan oleh user.
- Static vs Dynamic testing
	- Static testing berarti melakukan testing tanpa melakukan pemrograman, dan umumnya dapat dilakukan di semua fase.
	 - Dynamic testing berarti melakukan testing dengan tujuan meng-evaluasi dan mengobservasi *behaviour* product, dan umumnya dilakukan saat *runtime*.
- Black-box vs White-box testing
	- Black-box Testing berarti melakukan test pada suatu sistem tanpa pengetahuan atau tanpa informasi soal cara kerjanya sebelumnya. Seorang *tester* harus memberikan sebuah input dan melihat output yang dihasilkan oleh sistem. (Equivalence Partitioning)
	- White-box testing atau clear, glass box, atau structural testing. Merupakan teknik testing yang meng-evaluasi *code* dan cara kerja sebuah program. (Basis Path Testing)
- Software Testing Stages.
	- Unit Testing (*testing* terhadap masing masing komponen).
	- Module Testing (*testing* sebuah *collection* dari komponen-komponen yang saling berhubungan).
	- Sub-system Testing (*testing* sebuah *collection* dari module-module yang saling berintegrasi dalam sebuah *sub-system*).
	- System Testing (*testing* sistem secara penuh dan keseluruhan sebelum *deployment*).
	- Acceptance Testing (*testing* yang dilakukan oleh user untuk melihat apakah sistem memenuhi keinginan user). Atau biasa dikenal juga sebagai (Alpha / Beta testing). Alpha testing umumnya dilakukan di lingkup internal, dan Beta testing dilakukan di lingkup eksternal.
- Miscellaneous Testing.
	- Stress Testing, *testing* ini digunakan untuk menguji program seberapa tahan ketika diminta *resources* dalam jumlah yang banyak dan tidak biasa.
	- Recovery Testing, *testing* sistem yang memaksa program untuk gagal / *error* sehingga *recovery* dapat dilakukan dengan baik.
	- Security Testing *testing* untuk menguji mekanisme perlindungan dari sebuah sistem.
	- Performance Testing *testing* untuk menguji *run-time performance* dari sebuah software.
	- Compatibility Testing *testing* untuk menguji apakah program dapat dijalankan di hardware, *operating system*, aplikasi, *network environments* yang berbeda.
	- Usability Testing *testing* untuk menguji seberapa mudah sebuah *design* digunakan oleh kelompok demografi user.
- Test Automation.
	- Adalah teknik untuk menggunakan *software* lain untuk melakukan *testing* pada sebuah program.
	- Umumnya digunakan untuk mengontrol proses eksekusi dari test dan membandingkan hasil output yang terjadi dan hasil output yang diharapkan.
	- *Test automation* penting dalam proses CI/CD atau *Continuous Integration and Continuous Delivery*
	- Contohnya adalah:
		- Regression testing adalah *testing* yang menjalankan ulang test yang fungsional dan non-fungsional untuk memastikan software yang sudah ditest sebelumnya tidak mengalami perubahan.
## Summary
- Lakukan Testing seawal mungkin
- Testing adalah aktivitas yang terus menerus
- Saat mendesain software, sebaiknya di desain untuk *test*-able
- *Test activities* sebaiknya di rencanakan, kontrol, dan dokumentasi dengan baik baik.
