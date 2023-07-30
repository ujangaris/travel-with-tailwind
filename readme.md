# Travel App with TailwindCSS

## setup project with tailwind

    Todo:
    1.  setup project
        - npm init -y
    2.  install tailwind
        - docs: https://tailwindcss.com/docs/installation
        - npm install -D tailwindcss
        - npx tailwindcss init
        - content: ["./src/**/*.{html,js}"],
    3.  src/index.html
        - ini halaman utama dari aplikasi ini
        - buat h1 dengan class text-red-600 isinya Hello World
    4.  src/input.css
        - pasang code berikut:
            @tailwind base;
            @tailwind components;
            @tailwind utilities;
        - kemudian jalankan code berikut:
            npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
    5.  buat file .gitignore
        - daftarkan folder node_modules
    6.  jalankan aplikasi
        - klik kanana pada file index.html
        - pilih open with live server
        - akan tampil tulisan Hello World dengan warna merah

## setup font

    Todo:
    1.  public/font/CircularStd-Bold.ttf
        - siapkan font CircularStd-Bold.ttf
    2.  src/input.css
        - setup font yang sudah disiapkan pada file publi/font
        - setup agar setiap h1 menggunakan Circular STD
    3.  src/index.html
        - - buat h1 dengan class text-red-600 isinya Hello World
    4.  jalankan aplikasi
        - klik kanana pada file index.html
        - pilih open with live server
        - akan tampil tulisan Hello World dengan warna merah
        - inspek elemet huruf h1, (font nya adalah CircularStd)
          seperti yang sudah kita setup, jika semua h1 font nya CircularStd
    5.  src/index.html
        - font google
          pasang link dari font google inter
        - pasang p dan span
    6.  src/input.css
        - setup agar semua menjadi font inter
    7.  tailwind.config.js
        - setup fontFamily menjadi inter
    9.  jalankan aplikasi
        - klik kanana pada file index.html
        - refresh halaman
        - pada tulisan selain tulisan Hello World dengan warna merah
        - inspek elemet , (font nya adalah inter)
          seperti yang sudah kita setup, jika semua font nya menjadi inter

## setup colors

    Todo:

    1.  tailwind.config.js
        - tambahkan colors
          kemudian tambahkan color apa saja yang mau dijadikan default setup  key dan value nya:
            - ungu: "#5D50C6",
            - pink: "#F85E9F",
            - orange: "#FF5722",
    2.  src/index.html
        - isi clas pada h1, p, dan span dengan class color yang sudah kita buat diatas
    3.  jalankan aplikasi
        - klik kanana pada file index.html
        - refresh halaman
        - pada halaman utama akan ada :
            - Hello World berwarna orange
            - Coba berwarna pink
            - coba font berwarna ungu

## Mobile view - Menu atas & menu bawah

    Todo:

    1.  setup runing application
        - package.json
          - pada script tambahkan code berikut:
            "scripts": {
                "dev": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch",}
          - cara menjalankannya : npm run dev
          - buka index.html klik kanan trus open with live server
    2.  public/assets/
        - export image dari figma pada bagian menu untuk tampilan mobile dalam bentuk svg
        - namakan dengan nama logo dan toggle
    3.  src/index.html
        - menu atas:
            - pasang svg logo & toggle
        - menu bawah:
            - pasang cdn ionicon pada bagian bawah sebelum tutup body
            - pasang icon pada bagian yang dibutuhkan
            - docs: https://ionic.io/ionicons/usage
    4.  tailwind.config.js
        - pasang warna grey(ini hanya penamaan) untuk warna tulisan yang diambil dari design figma
          agar dpt digunakan pada tailwind
    5.  pada browser: akan ada menu atas dan bawah

## Mobile view - menu login & sign up

    Todo:

    1.  src/index.html
        - button login & sign up
            - 'left-1/2' artinya left 50%
            - '-translate-x-1/2' artinya bergeser 50%
            'w-3/4' artinya sebesar 75%
    2.  pada browser: akan ada menu atas dan bawah

## Mobile view - menampilkan dan menghilangkan menu login & sign up

    Todo:

    1.  src/index.html
        - pasang cdn alpain js
        - x-data="{open:false}" pada bagian pembungkus
        - @click="open = !open" pada bagian button yang akan di clik
        - tambahakan animation pada bagian menu yang akan muncul dan menghilang
        - dosc: https://alpinejs.dev/directives/transition
    2.  pada browser:
        - klik menu more, maka akan muncul menu login & signup
        - jika di klik lagi akan menghilang
        - menu muncukl dengan soft ( karna animation yang dipasang dengan alpainjs)

## Mobile view - menampilkan dan menghilangkan menu

    Todo:

    1.  src/index.html
        - x-data="{open:true}" pada bagian pembungkus
        - @click="open = !open" pada bagian button yang akan di clik
        - tambahakan animation pada bagian menu yang akan muncul dan menghilang
        - dosc: https://alpinejs.dev/directives/transition
    2.  pada browser:
        - klik menu burger dipojok kanan atas, maka akan muncul menu dibagian bawah aplikasi
        - jika di klik lagi akan menghilang
        - menu muncukl dengan soft ( karna animation yang dipasang dengan alpainjs)

## Tablet view - rubah posisi menu dengan class order

    Todo:

    1.  src/index.html
        - order-1 artinya posisi pertama order-2 posisi kedua order-3 posisi ketiga
        - sm:order-1 pada layar small posisi pertama sm:block akan ditampilkan penuh pada ukuran layar small
        - class="order-3 hidden sm:block" artinya akan dihilangkan di ukuran layar small
        - dosc: https://tailwindcss.com/docs/order
    2.   jalankan aplikasi agar semua perubahan berjalan dengan semestinya
        - npm run dev
    3.  pada browser:
        - pada ukuran layar tablet bar menu di urutan pertama di ikuti dengan logo
          dan pada urutan terakhir adalah  button login dan sign up
        - jika pada ukuran small(sm) menu login sign up akan hilang,
          dan urutan pertama logo kemudian di ikuti dengan menu burger

## Dekstop/laptop view - menu Home , Discover, Special Deals & Contact

    Todo:

    1.  src/index.html
        - class="order-2 hidden lg:block" artinya akan tampil hanya dilayar large dengan urutan kedua setelah logo
          dan akan hilang di kurusan selain large
        - items-center agar sejajar dengan menu lainnya
        - <img class="lg:hidden order-2 sm:order-1"/> lg:hiden artinya akan hilang di ukuran larayar large
        - dosc: https://tailwindcss.com/docs/order
    2.  tailwind.config.js
        - tambahkan font Circular STD agar dapat digunakan
    3.   jalankan aplikasi agar semua perubahan berjalan dengan semestinya
        - npm run dev
    4.  pada browser:
        - pada ukuran layar laptop/dekstop menu Home, Discover dll akan muncul di posisi ke dua
          setelah logo
        - jika pada ukuran selain large menu Home, Discover dll akan menghilang
