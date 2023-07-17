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
    5.  jalankan aplikasi
        - klik kanana pada file index.html
        - pilih open with live server
        - akan tampil tulisan Hello World dengan warna merah
