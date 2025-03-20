# Commit 1 Reflection Notes

Commit 1 menjelaskan langkah-langkah awal dalam membangun web server sederhana menggunakan Rust, mulai dari mendengarkan koneksi TCP hingga membaca permintaan HTTP dari klien. Dengan memanfaatkan TcpListener, server dapat menerima koneksi masuk, sementara TcpStream digunakan untuk membaca data dari klien. Proses parsing permintaan HTTP dilakukan dengan BufReader, yang membantu membaca baris demi baris hingga permintaan lengkap diterima. Output yang ditampilkan di terminal menunjukkan detail permintaan HTTP yang dikirim oleh browser, termasuk metode, header, dan metadata lainnya. Hal ini membantu memahami bagaimana komunikasi antara klien dan server berlangsung serta bagaimana browser berulang kali mencoba menghubungi server ketika tidak mendapatkan respons.

# Commit 2 Reflection Notes

![Commit 2 screen capture](/assets/images/commit2.png)

Modifikasi fungsi handle_connection memungkinkan server Rust menampilkan halaman HTML di browser dengan membaca dan mengirimkan file hello.html sebagai respons HTTP. Saya belajar bahwa dalam membangun server sederhana, penting untuk memahami cara menangani permintaan HTTP, membaca file secara dinamis, serta mengatur header seperti Content-Length agar browser dapat merender halaman dengan benar. Selain itu, memastikan tidak ada instance server sebelumnya yang masih berjalan sebelum menjalankan ulang sangat krusial untuk menghindari konflik port.

# Commit 3 Reflection Notes

![Commit 3 screen capture](/assets/images/commit3.png)

Perubahan pada handle_connection membuat server lebih fleksibel dengan memproses permintaan secara berbeda berdasarkan URL yang diminta. Saya belajar bagaimana menangani permintaan HTTP secara lebih spesifik dengan memeriksa baris pertama dari request. Jika klien meminta /, server akan mengirimkan halaman utama, sedangkan untuk permintaan lainnya, server akan merespons dengan kode status 404 NOT FOUND dan halaman error. Ini mengajarkan pentingnya menangani berbagai kemungkinan permintaan untuk meningkatkan pengalaman pengguna dan mencegah error yang tidak ditangani dengan baik.