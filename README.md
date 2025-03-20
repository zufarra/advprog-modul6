# Commit 1 Reflection Notes

Commit 1 menjelaskan langkah-langkah awal dalam membangun web server sederhana menggunakan Rust, mulai dari mendengarkan koneksi TCP hingga membaca permintaan HTTP dari klien. Dengan memanfaatkan TcpListener, server dapat menerima koneksi masuk, sementara TcpStream digunakan untuk membaca data dari klien. Proses parsing permintaan HTTP dilakukan dengan BufReader, yang membantu membaca baris demi baris hingga permintaan lengkap diterima. Output yang ditampilkan di terminal menunjukkan detail permintaan HTTP yang dikirim oleh browser, termasuk metode, header, dan metadata lainnya. Hal ini membantu memahami bagaimana komunikasi antara klien dan server berlangsung serta bagaimana browser berulang kali mencoba menghubungi server ketika tidak mendapatkan respons.

# Commit 2 Reflection Notes

![Commit 2 screen capture](/assets/images/commit2.png)

Modifikasi fungsi handle_connection memungkinkan server Rust menampilkan halaman HTML di browser dengan membaca dan mengirimkan file hello.html sebagai respons HTTP. Saya belajar bahwa dalam membangun server sederhana, penting untuk memahami cara menangani permintaan HTTP, membaca file secara dinamis, serta mengatur header seperti Content-Length agar browser dapat merender halaman dengan benar. Selain itu, memastikan tidak ada instance server sebelumnya yang masih berjalan sebelum menjalankan ulang sangat krusial untuk menghindari konflik port.