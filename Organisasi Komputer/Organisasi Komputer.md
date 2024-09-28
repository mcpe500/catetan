# Pertemuan 1
Pada dasarnya, komputer tidak mengerti perintah-perintah yang diberikan oleh manusia, seperti: *print*, yang komputer mengerti adalah biner / machine language, namun untuk menggunakan biner akan menyulitkan manusia sehingga kita membuat *hexadecimal*

Namun meskipun begitu, instruksi dalam *hexa* yang bekerja untuk mikro-prosesor A mungkin tidak akan bekerja untuk mikro-prosesor B, instruksi untuk mikro-prosesor *x_86* mungkin tidak akan bekerja untuk mikroprosesor *ARM*

Sehingga kita memerlukan *compiler* atau *interpreter* yang bisa digunakan untuk menerjemahkan instruksi ke instruksi masing-masing mikroprosesor.

Meskipun begitu, kenyataannya mikro-prosesor yang dibuat ada sangat banyak sehingga tidak memungkinkan untuk mengingat semua instruksi mikro-prosesor yang belum tentu banyak dipakai sehingga untuk ini kita dapat menggunakan *Assembly Language* yang berbeda dengan *Machine Language*. *Assembler* menerjemahkan *Assembly Language* melalui interpreter ke *Machine Language*.
