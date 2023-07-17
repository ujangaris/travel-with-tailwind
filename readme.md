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
