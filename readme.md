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
    4.  tailwind.config.js
        - pasang warna grey(ini hanya penamaan) untuk warna tulisan yang diambil dari design figma
          agar dpt digunakan pada tailwind
    5.  pada browser: akan ada menu atas dan bawah
