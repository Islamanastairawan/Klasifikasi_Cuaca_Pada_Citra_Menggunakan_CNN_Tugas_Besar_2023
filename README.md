## Keterangan

Kode ini merupakan implementasi Convolutional Neural Network (CNN) untuk memprediksi kondisi cuaca berdasarkan citra menggunakan TensorFlow dan scikit-image.

Kode ini memiliki beberapa fungsi utama, antara lain:

1. `load_images_from_folder(folder)`: Memuat citra dari folder yang ditentukan dan mengembalikan daftar citra.
2. `resize_images(images)`: Mengubah ukuran citra menjadi 224x224 piksel.
3. `convert_to_rgb(images)`: Mengkonversi citra menjadi format RGB.
4. `normalize_images(images)`: Normalisasi nilai piksel citra ke rentang 0-1.
5. `convert_to_gray(images)`: Mengkonversi citra RGB menjadi citra grayscale.
6. `preprocess_images(images)`: Melakukan serangkaian langkah pra-pemrosesan pada citra, termasuk resize, konversi ke RGB, normalisasi, dan konversi ke grayscale.
7. `predict_weather(image_folder, num_samples=3)`: Memuat citra cuaca dari folder yang ditentukan, melakukan pra-pemrosesan, dan memprediksi kondisi cuaca menggunakan model CNN yang telah dilatih. Juga menampilkan citra beserta properti GLCM (Gray-Level Co-occurrence Matrix) seperti dissimilarity, ASM, contrast, correlation, energy, dan homogeneity.

Selain itu, kode ini juga melibatkan proses berikut:

1. Memuat citra dari masing-masing kategori cuaca (berawan, hujan, cerah, matahari terbit) dan melakukan pra-pemrosesan pada citra-citra tersebut.
2. Menggabungkan semua citra ke dalam satu array dan menyusun label untuk masing-masing citra.
3. Membagi dataset menjadi data latih dan data uji dengan perbandingan 80:20.
4. Membangun model CNN dengan lapisan-lapisan konvolusi dan lapisan-lapisan terhubung penuh.
5. Melatih model menggunakan data latih.
6. Menguji model menggunakan data uji dan menghitung akurasi pengujian.

Informasi lebih lanjut dapat ditemukan dalam komentar di dalam kode.
