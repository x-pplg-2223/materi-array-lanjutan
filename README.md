# Array

## Apa itu Array?
Array adalah kumpulan atau tumpukan berbagai data. Cara menuliskan array yaitu dengan kurung siku ([]) dan elemen-elemen nya dipisah menggunakan tanda koma (,). Setiap elemen dari array memiliki indeks yang dimulai dari 0, 1, 2, dst. Kita dapat memanipulasi array dengan berbagai cara seperti menambahkan dan mengeluarkan elemen dalam array, menggabungkan array, atau bahkan menghapus seluruh elemen Array nya. Kita bisa memasukkan beberapa tipe data yang berbeda ke dalam Array bahkan memasukkan Array ke dalam Array.

Array juga memiliki property **.length** seperti pada string yang berarti panjang dari sebuah array.

```js
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

Cara menggunakan metode array adalah dengan menggunakan tanda dot (.) contohnya sbb:

```js
var feeling = ["dag", "dig"]
feeling.push("dug") // menambahkan nilai "dug" ke index paling belakang
feelling.pop() // menghapus nilai pada elemen terakhir array
```

Beberapa metode array ada yang mengembalikan nilai array lama yang sudah diperbarui (array lama di-update) dengan metode tersebut , dan ada pula metode array yang mengembalikan sebuah array baru dan tidak mengubah data pada array yang lama (array baru yang serupa dengan array lama). Sifat seperti ini disebut mutable atau immutable.

### **.push()**
*Push* adalah metode array untuk menambahkan nilai di belakang elemen terakhir di array. metode push menerima sebuah parameter yaitu nilai yang ingin kita tambahkan ke dalam array.

```js
var numbers = [0, 1, 2]
numbers.push(3)
console.log(numbers) // [0, 1, 2, 3]
// Bisa juga memasukkan lebih dari satu nilai menggunakan metode push
numbers.push(4, 5)
console.log(numbers) // [0, 1, 2, 3, 4, 5] 
```
### **.pop()**
*Pop* adalah kebalikan dari push yaitu menghapus nilai elemen paling terakhir dari sebuah array. metode Pop tidak menerima parameter apapun sehingga metode pop hanya bisa mengeluarkan satu elemen saja yaitu yang paling terakhir dari sebuah array.

```js 
var numbers = [0, 1, 2, 3, 4, 5]
numbers.pop() 
console.log(numbers) // [0, 1, 2, 3, 4] 
``` 

### **.unshift()**
*Unshift* yaitu menambahkan nilai pada index ke-0 sehingga elemen-elemen sebelumnya bergeser.

```js
var numbers = [0, 1, 2, 3]
numbers.unshift(-1) 
console.log(numbers) // [-1, 0, 1, 2, 3]
``` 

### **.shift()**
**Shift** kebalikan dari unshift yaitu menghapus nilai pada elemen terdepan dari sebuah array. metode Shift tidak menerima parameter apapun.

```js
var numbers = [ 0, 1, 2, 3]
numbers.shift()
console.log(numbers) // [1, 2, 3] 
``` 

## **.sort()**
**Sort** adalah metode untuk mengurutkan nilai pada array. Secara otomatis, sort akan mengurutkan secara ascending (dari rendah ke tinggi) dan diurutkan berdasarkan unicode dari karakter. Urutan unicode artinya ada karakter yang secara nilai lebih besar dibandingkan dengan karakter yang lainnya. contohnya adalah karakter "b" akan lebih besar daripada "a", karakter "c" lebih besar daripada karakter "b", dst.

```js
var animals = ["kera", "gajah", "musang"] 
animals.sort()
console.log(animals) // ["gajah", "kera", "musang"]
``` 

### *.slice()*
**slice** adalah metode untuk mengambil irisan dari sebuah array. Metode slice bisa menerima satu atau dua parameter. Parameter pertama adalah nomer index pertama yang akan kita ambil sebagai irisan, sedangkan parameter kedua adalah nomer index terakhir yang ingin kita ambil sebagai irisan.

```js
var angka = [0, 1, 2, 3]
var irisan1 = angka.slice(1,3) 
console.log(irisan1) //[1, 2]
var irisan2 = angka.slice(0,2)
console.log(irisan2) //[0, 1] 
``` 

Jika parameter kedua tidak diisi maka secara otomatis slice akan mengiris array dari indeks di paramer pertama sampai ke indeks terakhir array tersebut.

```js
var angka = [0, 1, 2, 3]
var irisan3 = angka.slice(2)
console.log(irisan3) // [2, 3] 
```

Jika diperhatikan, metode slice tidak mengubah Array yang awal dan hasil irisan array dapat kita tampung kembali ke variable yang baru. Oleh karena itu metode Slice juga berfungsi untuk membuat salinan atau "shallow copy" dari sebuah array. Cara membuat shallow copy dengan metode slice yaitu dengan tanpa memberikan parameter apapun pada metode slice.

```js
var angka = [0, 1, 2, 3]
var salinAngka = angka.slice()
console.log(salingAngka) // [0, 1, 2, 3]
```

### *.splice()*
*Splice* yaitu metode untuk menghapus dan/atau menambahkan nilai elemen pada array. Metode splice bisa menerima parameter sebanyak dua atau lebih parameter. Jika ingin menggunakan splice untuk menghapus elemen pada index tertentu maka digunakan 2 paramater. Jika ingin menggunakan splice untuk menambahkan elemen pada index tertentu maka digunakan tiga parameter.
```js
array.splice([IndexMulai], [JumlahNilaiYangDihapus], [NilaiYangDitambahkan1], [NilaiYangDitambahkan2], ...);
```

Berikut contoh penggunaan metode *splice()*
```js
var fruits = [ "banana", "orange", "grape"]
fruits.splice(1, 0, "watermelon") 
console.log(fruits) // [ "banana", "watermelon", "orange", "grape"]
```

Contoh di atas berarti kita mulai mengubah array fruits dari indeks no 1, dan melakukan penghapusan nilai sebanyak 0 (yang berarti tidak menghapus apapun), dan menambahkan nilai "watermelon" pada indeks tersebut.

```js
var fruits = [ "banana", "orange", "grape"]
fruits.splice(0, 2)
console.log(fruits) // ["grape"]
```

Contoh di atas berarti kita mulai mengubah array fruits dari indeks ke-0 dan melakukan penghapusan data sebanyak 2 elemen.

### *.split()* dan *.join()*
 
Metode split yaitu memecah sebuah string sehingga menjadi sebuah array. Split menerima sebuah parameter berupa karakter yang menjadi separator untuk memecah string.

```js
var biodata = "name:john,doe" 
var name = biodata.split(":")
console.log(name) // [ "name", "john,doe"] 
```

Metode join yaitu kebalikan dari split yaitu mengubah sebuah array menjadi string dengan cara menggabungkan (join) seluruh elemen array menjadi satu dengan sebuah karakter pemisah yang dikirim melalui parameter. contohnya sebagai berikut:

```js
var title = ["my", "first", "experience", "as", "programmer"] 
var slug = title.join("-")
console.log(slug) // "my-first-experience-as-programmer"
```