# Array

## Apa itu Array?
Array adalah kumpulan atau tumpukan berbagai data. Cara menuliskan array yaitu dengan kurung siku ([]) dan elemen-elemen nya dipisah menggunakan tanda koma (,). Setiap elemen dari array memiliki indeks yang dimulai dari 0, 1, 2, dst. Kita dapat memanipulasi array dengan berbagai cara seperti menambahkan dan mengeluarkan elemen dalam array, menggabungkan array, atau bahkan menghapus seluruh elemen Array nya. Kita bisa memasukkan beberapa tipe data yang berbeda ke dalam Array bahkan memasukkan Array ke dalam Array.

Array juga memiliki property **.length** seperti pada string yang berarti panjang dari sebuah array.

```html
var hobbies = ["coding", "cycling", "climbing", "skateboarding"] 
console.log(hobbies) // [ 'coding', 'cycling', 'climbing', 'skateboarding' ]
console.log(hobbies.length) // 4 
 
console.log(hobbies[0]) // coding
console.log(hobbies[2]) // climbing
// Mengakses elemen terakhir dari array
console.log(hobbies[hobbies.length -1] // skateboarding
```

## Metode Array
Berikut ini adalah beberapa metode atau built-in functions yang dimiliki oleh tipe data array:
- push: menambah 1 nilai ke array ke index paling belakang
- pop: menghapus 1 nilai dari array index paling belakang
- unshift: menambah 1 nilai ke array index paling depan (index 0)
- shift: menghapus 1 nilai dari array index paling depan (index 0)
- join: menggabungkan seluruh element array menjadi sebuah string dan mengambil parameter sebagai simbol penyambung antar elemen
- sort: mengurutkan elemen di dalam array sesuai alphabet
- slice: mengambil beberapa lapis data
- splice: mengubah nilai array dengan menghapus dan/atau menambah nilai baru ke array
- split: memecah string dan mengembalikan array sesuai dengan separator / pemisah yang didefinisikan