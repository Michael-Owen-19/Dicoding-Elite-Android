# Technical Exercise Result (Android 3)

### Project name: Submission StoryApp

## Project Summary

- Kode yang tidak pernah digunakan baik itu Class, method, ataupun variable jika tidak digunakan sebaiknya dihapus. Kamu bisa memanfaatkan **Analyze - Code Cleanup** untuk melakukannya dengan cepat.
- Sebaiknya gunakan versi terbaru dari setiap dependensi dan plugin yang digunakan sesuai dengan best practice yang disarankan
- Perhatikan penggunaan layout dan desain tampilan yang digunakan sehingga tidak mengganggu experience pengguna saat menggunakan aplikasi anda.
- Anda dapat mengubah ikon aplikasi yang anda gunakan sehingga tampilan aplikasi menjadi lebih menarik.

## Error Notes

Pada project yang diperiksa terjadi sebuah error saat menjalankan aplikasi yakni terjadi gagal build akibat google maps api key yang belum terisi pada file android manifest dan Saya mengatasinya dengan cara menambahkan google maps api key yang valid.

## Code Review

```kotlin
...
implementation 'androidx.lifecycle:lifecycle-viewmodel-ktx:2.6.1'
implementation 'androidx.lifecycle:lifecycle-livedata-ktx:2.6.1'
implementation 'androidx.activity:activity-ktx:1.7.2'
implementation 'com.google.android.gms:play-services-maps:18.1.0'
implementation "androidx.paging:paging-runtime-ktx:3.2.0"
...
```

> Selalu gunakan versi terbaru dari Kotlin Plugin dan dependensi yang anda gunakan agar kode yang Anda tuliskan sesuai dengan best practice yang disarankan. Silahkan update pada file **build.gradle** level module.
> 

```kotlin
fun rotateBitmap(bitmap: Bitmap, isBackCamera: Boolean = false): Bitmap {
			...
	}
```

> Kode yang tidak pernah digunakan baik itu Class, method, ataupun variable jika tidak digunakan sebaiknya dihapus. Kamu bisa memanfaatkan **Analyze - Code Cleanup** untuk melakukannya dengan cepat.
> 

![WhatsApp Image 2024-05-07 at 18.01.46_6df03fae.jpg](Technical%20Exercise%20Result%20(Android%203)%20d6f9a4955449485a8491a57dd1f5c34c/WhatsApp_Image_2024-05-07_at_18.01.46_6df03fae.jpg)

> Pada Halaman Detail tampilan masih terpotong saat orientasi diubah menjadi landscape. Anda dapat menggunakan Scroll View Layout pada halaman detail untuk menampilkan informasi dengan baik saat orientasi diubah menjadi landscape.
>