# Array

## Apa itu Array?
<p align='justify'>Array adalah kumpulan atau tumpukan berbagai data. Cara menuliskan array yaitu dengan kurung siku ([]) dan elemen-elemen nya dipisah menggunakan tanda koma (,). Setiap elemen dari array memiliki indeks yang dimulai dari 0, 1, 2, dst. Kita dapat memanipulasi array dengan berbagai cara seperti menambahkan dan mengeluarkan elemen dalam array, menggabungkan array, atau bahkan menghapus seluruh elemen Array nya. Kita bisa memasukkan beberapa tipe data yang berbeda ke dalam Array bahkan memasukkan Array ke dalam Array.</p>

Array juga memiliki property *.length* seperti pada string yang berarti panjang dari sebuah array.

```html
var hobbies = ["coding", "cycling", "climbing", "skateboarding"] 
console.log(hobbies) // [ 'coding', 'cycling', 'climbing', 'skateboarding' ]
console.log(hobbies.length) // 4 
 
console.log(hobbies[0]) // coding
console.log(hobbies[2]) // climbing
// Mengakses elemen terakhir dari array
console.log(hobbies[hobbies.length -1] // skateboarding
```