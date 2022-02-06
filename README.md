# 1. Struktur Folder
Open `“vue-project”` menggunakan code editor, pada tutorial ini saya menggunakan `Visual Studio Code`. Saya juga menyarankan Anda untuk menggunakan `Visual Studio Code`.

Jika Anda perhatikan lebih detail, maka Anda akan mendapatkan struktur folder seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152677472-0a03b809-5545-4f3a-a12f-66746eaab4a1.png)

Pada gambar diatas, terdapat 3 folder yaitu: folder `node_modules`, `public`, dan `src`.

Folder node_modules berisi semua modul yang dibutuhkan dalam pembuatan project.

Folder public berisi file index.html dan favicon.ico, file index.html merepresentasikan Single Page Application (SPA).

Folder src berisi file App.vue, main.js, folder assets, dan folder components.

File App.vue merupakan file induk dari aplikasi vue js, file main.js merupakan penghubung antara file App.vue dan index.html.

Folder assets merupakan folder yang berisi images atau resources lainnya yang dibutuhkan dalam membangun aplikasi.

Sedangkan folder components merupakan folder yang akan berisi semua komponen yang dibutuhkan dalam membangun aplikasi.

Secara default, terdapat satu komponen yaitu `HelloWorld.vue`.

Silahkan hapus file komponen `HelloWorld.vue`, karena kita tidak membutuhkannya, kemudian ubah kode pada `App.vue` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152677668-abbf894c-9db9-4b1c-a5af-bf3a093bbfc9.png)

# 2. Data dan Methods

Vue.js memberikan kemudahan dalam menampilkan data secara dinamis.

Untuk lebih jelasnya silahkan ketikan kode berikut pada file `“App.vue”`:

![image](https://user-images.githubusercontent.com/92959023/152677745-a42d5cb6-35db-48e0-9587-5e366eb19051.png)

Kemudian kembali ke browser, maka Anda akan melihat hasil seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152677799-20117258-8aec-4ac9-950e-8f328c0cef66.png)

Anda juga dapat mengubah datanya melalui method.

Ubah kode `“App.vue”` menjadi seperti berikut untuk lebih jelasnya:

![image](https://user-images.githubusercontent.com/92959023/152677854-bc3eedb2-7560-4a6b-a0e4-57b0c766258e.png)

Pada kode diatas terdapat methods, dimana didalamnya terdapat satu function yaitu changeName() yang berfungsi untuk mengganti value dari property data name menjadi “Jhon Thomas”.

Function changeName dipanggil ketika tombol `“Change Name”` di klik.

Kembali ke browser, kemudian klik tombol “Change Name”.

Jika berjalan dengan baik, maka `“Muhammad Farhan”` akan berubah menjadi `“Jhon Thomas”` seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152677971-dfb1705a-431f-40d5-b061-e6470e9f2a5d.png)

# 3. Data Binding
Data binding merupakan fitur penting yang wajib Anda ketahui dalam membangun aplikasi vue.js.

Anda dapat mem-binding artribut, class, dan sebagainya.

Sebagai contoh disini saya ingin mem-binding artibut `href` pada tag anchor.

Ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152678040-4a62ae3e-ea7e-43cd-aa75-ce338ee9c32b.png)

Jika Anda perhatikan kode diatas, terdapat tag `<a>` dengan atribut `href` mengambil valuenya dari property data `“url”`.

Anda TIDAK dapat membuatnya seperti ini:

![image](https://user-images.githubusercontent.com/92959023/152678178-222b5b89-06ec-4922-b3a3-28592cbb5581.png)

Ataupun seperti ini:

![image](https://user-images.githubusercontent.com/92959023/152678201-c8525f3e-89b1-416b-bf66-e812fe87c856.png)

Itulah kenapa Anda membutuhkan data binding. Dengan memanfaatkan data binding, Anda dapat membuat atribut ataupun class menjadi dinamis.

# 4. Two-Way Data Binding

Vue menyediakan fitur two-way data binding yang berfungsi untuk mengambil value dari input form.

Berbeda dari mengambil value dari input form pada umumnya, two-way data binding berlaku dua arah.

Untuk lebih jelasnya, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152678335-8b451b89-e07d-4d29-9fab-ac34ca172f40.png)

Pada kode diatas terdapat satu input text dengan atribut two-way data binding yaitu: `“v-model”`.

Pada property data terdapat name dengan string kosong untuk default value-nya.

Kembali ke browser, jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152678440-987e6f36-b5d1-41f7-9c92-22067f7e3caf.png)

Pada gambar diatas, Anda dapat melihat setiap kali saya mengetikan sesuatu pada input text, maka secara otomatis akan sama pada outputnya.

Ini tidak hanya berlaku dari input text ke property data, tetapi juga berlaku sebaliknya.

Jika Anda masukan value pada property data name=”Jhon”, maka secara otomatis pada input text juga berisi “Jhon”.

Two-way data binding ini sangat bermanfaat jika Anda bekerja dengan form.

 # 5. Conditionals dan Loops
Anda dapat menggunakan kondisi if dengan `“v-if”` directive, dan Anda juga dapat membuat perulangan menggunakan `“v-for”` directive pada vue.js.

Untuk lebih jelasnya, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152679841-34077b82-9514-4cfe-9c3c-9b841630a1b3.png)

Pada kode diatas, Anda dapat melihat bahwa kita menggunakan `“v-if”` dan `“v-for”` secara bersamaan.

`“v-for”` berfungsi untuk melakukan perulangan pada property data products, sedangkan `“v-if”` berfungsi untuk menampilkan data jika terdapat data dan menampilkan pesan `“No Data”` jika tidak ada data.

Pada kasus diatas, kita hanya menggunakan data statis. Akan tetapi pada kasus sebenarnya data tersebut bisa berasal dari backend API.

Kembali ke browser untuk memastikan tidak terdapat error.

Jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152680078-d0051ca8-08cf-49de-984d-911cf5ca0cbe.png)

# 6. Lifecycle Hooks

Salah satu hal yang sangat penting untuk Anda ketahui di vue.js adalah lifecycle hooks.

Lifecycle hooks adalah jendela bagaimana library yang Anda gunakan bekerja di balik layar. Lifecycle hooks memungkinkan Anda mengetahui kapan komponen Anda dibuat, ditambahkan ke DOM, diperbarui, atau dihancurkan.

Ada banyak lifecycle hooks pada vue.js seperti created, beforeCreate, mounted, beforeMount, updated, beforeUpdate, dan lainnya.

Pada tutorial ini, saya hanya akan memanfaatkan satu lifecycle hooks yaitu: `created`.

Lifecycle hooks `“created”` merupakan lifecycle hooks yang pertama kali dijalankan setelah initialize component dan memungkinkan Anda mengakses reactive data dan event sebelum template dan Virtual DOM mounted dan rendered.

Mungkin terlihat membingungkan, tapi sebenarnya tidak.

Untuk lebih jelasnya, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152680028-79b393bf-988d-497e-b8ae-41b5f018d8ed.png)

Pada kode diatas, dapat dilihat bahwa pada property data terdapat products dengan empty array.

Sementara datanya, di pindahkan ke lifecycle hooks created. Hal ini berfungsi agar data di load sebelum Virtual DOM rendered ke DOM.

Jika Anda ingin menjalankan function yang sebelum Virtual DOM rendered, maka Anda dapat menempatkan function tersebut ke lifecycle hooks created.

Jika Anda kemball ke browser, maka semuanya masih berjalan seperti sebelumnya.

![image](https://user-images.githubusercontent.com/92959023/152680438-1a837197-da0c-4488-8e06-ec9e88b6dfd8.png)

# 7. Computed Properties
Computed property adalah property yang dapat Anda gunakan untuk mendefiniskan data yang value tergantung dari data lain.

Sebagai contoh misalnya Anda ingin menampilkan data berdasarkan kata kunci tertentu seperti pencarian.

Untuk lebih jelasnya, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152680570-490e8ba0-1e83-429e-b800-618bf46bda59.png)
![image](https://user-images.githubusercontent.com/92959023/152680588-f605e458-9008-4e66-bf53-f16656a5a6d4.png)

Pada kode diatas, dapat dilihat bahwa terdapat satu input text yang berfungsi untuk percarian.

Pada logic terdapat computed property yang didalamnya terdapat satu function yaitu: filterProducts.

Function filterProducts berfungsi untuk melakukan percarian data berdasarkan title sama dengan kata kunci dari input text.

Kembali ke browser, jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152680719-08a8e6ba-a253-4419-a27b-172e2d318f64.png)

Jika Anda ingin mendefinisikan data yang nilai tergantung dari data lain, maka Anda dapat menggunakan computed property.

# 8. Components
Salah satu konsep penting yang harus Anda ketahui di vue.js adalah komponen.

Vue.js sering kali digunakan untuk membangun Single Page Application (SPA) dengan multiple komponen.

Untuk lebih jelasnya, buat file komponen bernama `“Header.vue”` di folder `“src/components”`.

Kemudian ketikan kode berikut:

![image](https://user-images.githubusercontent.com/92959023/152680922-0e805ea9-63c6-481b-b5ee-eb8e8ebb7a01.png)

Setelah itu, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152680962-5502c3c4-bd04-45b4-ac9d-b65397baca2c.png)

Pada kode diatas dapat dilihat bahawa untuk dapat menggunakan komponen “Header”, Anda perlu mengimport file komponen tersebut, kemudian mendaftarkan komponen di Components Property, setelah itu Anda dapat meng-output komponen tersebut ke DOM.  

Kembali ke browser, jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152681062-6a1e17b1-056c-461c-ace3-22a38abaf7c3.png)

# 9. Props
Props berfungsi untuk mengirim data atau value dari komponen Induk (Parent Components) ke komponen anak (Child Components).

Sebagai contoh, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152681155-86a3c99f-4946-4ab3-b622-b22680e789f1.png)

Kemudian ubah kode `"Header.vue"` pada folder `"src/components"` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152681221-3772d0c8-4916-4f8c-8b1d-878756d5a403.png)

Pada kode diatas, Anda dapat melihat terdapat property props yang menerima value TextHeader yang datang dari komponen induk yaitu `“App.vue”.`

Kembali ke browser, jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152681294-570b357a-0961-46e7-95a3-6d00abf3401e.png)

# 10. Custom Events
Berbeda dengan props, custom events berfungsi untuk mengirim data dari komponen anak (child components) ke komponen induk (parent components).

Sebagai contoh, ubah kode `“Header.vue”` pada folder `“src/components”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152681465-7a1a0b19-f80d-4209-90ef-0f771514c386.png)

Kemudian, ubah kode `“App.vue”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152681524-58dd54fd-433c-4877-a207-73126ac61637.png)

Kode diatas berfungsi untuk mengubah text header dari “Welcome to M Fikri” menjadi “Welcome To The Jungle”.

Dimana text “Welcome To The Jungle” berasal dari komponen anak (Child Components).

Kembali ke browser, kemudian klik tombol “Change Title”.

Jika berjalan dengan baik, maka text header akan berubah menjadi “Welcome To The Jungle” seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152681581-26dc91ca-9e71-4878-9f35-93655f64cf65.png)

# 11. Vue Router
Vue Router berfungsi untuk merender spesifik komponen dengan spesifik URL.

Berbeda dengan multiple page application, vue router tidak melakukan request ke server, melainkan merender komponen tertentu di sisi client.

Untuk menggunakan Vue Router pada vue.js menggunakan Vue CLI dapat dilakukan dengan mudah dengan membuat project baru.

Oleh sebab itu, buat project vue.js baru dengan perintah berikut pada CMD (Command Prompt) atau terminal:

`vue create vue-project`

Seperti gambar berikut

![image](https://user-images.githubusercontent.com/92959023/152682020-cc159d6d-e731-4d30-ba7f-8b314e92dd6f.png)

Dimana `“vue-router-project”` adalah nama project yang akan dibuat.

Pada gambar diatas, saya membuat project baru didalam direktori:

`C:/Users/acer/Documents/Tutorials`

Jika Anda membuat pada folder yang berbeda, Anda dapat menggunakan perintah CD (Change Directory) untuk menuju ke folder Anda.

Setelah menjalankan perintah diatas, maka akan tampil pilihan seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152682240-49207bf9-e957-4d8c-bf0f-209b6a6c40a2.png)

Pilih => "Manualy select features".

![image](https://user-images.githubusercontent.com/92959023/152682325-769273f2-e4ae-4d4c-a24c-5e7cdc648661.png)

Kemudian, pilih `“Choose Vue version, Babel, dan Router”` kemudian Enter.

![image](https://user-images.githubusercontent.com/92959023/152682411-6ee7ff19-11b6-4794-8bae-419d16552971.png)

Pilih Vue versi 3.x, kemudian Enter seterusnya.

Maka Vue CLI akan membuat project baru untuk Anda.

Jika instalasi selesai, buka project `“vue-router-project”` menggunakan Visual Studio Code, maka Anda akan mendapati struktur folder seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152687617-a3bd87f5-ea36-4f67-a0d2-77113b5c12ef.png)

Pada gambar diatas, terdapat penambahan 2 folder didalam folder `“src”` yaitu: `“router”` dan `“views”`.

Pada folder `“router”` terdapat file `“index.js”` yang berfungsi untuk mengontrol semua route dari project di bangun.

Sedangkan pada folder `“views”` terdapat file `“Home.vue”` dan `“About.vue”` yang berfungsi untuk tampilan atau halaman yang ingin Anda gunakan pada route.

Untuk memastikan semua project berjalan dengan baik, jalankan project dengan mengetikan perintah berikut pada terminal:

`npm run serve`

Jika berjalan dengan baik, maka akan terlihat seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152687901-9eb5b088-32f3-4e95-9715-edb892c120a0.png)

Pada gambar diatas terdapat menu `“Home”` dan `“About”.`

Anda dapat pergi ke halaman about dengan mengklik menu `“About”` atau mengunjungi URL berikut:

`http://localhost:8080/about`

Seperti gambar berikut:

![image](https://user-images.githubusercontent.com/92959023/152688055-6c1e9d0d-6c1e-4675-9dd1-6a2c69d5d030.png)

Selain itu, Anda juga dapat menambahkan halaman lainnya.

Sebagai contoh, buat file `“Contact.vue”` pada folder `“src/views”`, kemudian ketikan kode berikut:

![image](https://user-images.githubusercontent.com/92959023/152688233-e9b44b92-d389-4f31-96ec-3ac007ce5f87.png)

Kemudian ubah kode pada file `“index.js”` pada folder `“src/router”` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152688505-d11eaf5c-9fee-4b90-925e-41a9321a4628.png)

Setelah itu, ubah kode pada file `"App.vue"` menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/92959023/152688591-9dcaa6fd-2256-4942-bd29-8b84a13ec841.png)

Kembali ke browser, kemudian klik menu `“Contact”` atau kunjungi URL berikut:

`http://localhost:8080/contact`

Seperti gambar berikut

![image](https://user-images.githubusercontent.com/92959023/152688716-132761ea-63cb-4da2-8267-d19d47e1cb7b.png)

# Kesimpulan:
Pembahasan kali ini adalah tentang tutorial Vue.js 3 untuk pemula.

Pada tutorial ini, Anda telah belajar tentang apa itu vue.js, kenapa menggunakan vue.js, Vue CLI, hingga Vue Router.

Jadi tunggu apa lagi, let’s coding!
