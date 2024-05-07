# Technical Exercise Result (Android 4)

### Project name: Submission GithubUser

## Project Summary

- Kode yang tidak pernah digunakan baik itu Class, method, ataupun variable jika tidak digunakan sebaiknya dihapus. Kamu bisa memanfaatkan **Analyze - Code Cleanup** untuk melakukannya dengan cepat.
- Sebaiknya gunakan versi terbaru dari setiap library dan plugin yang digunakan sesuai dengan best practice yang disarankan
- Hindari penggunaan Hardcoded String, anda dapat manfaatkan Android String Resource.
- Perhatikan penggunaan layout dan desain tampilan yang digunakan sehingga tidak mengganggu experience pengguna saat menggunakan aplikasi anda.
- Anda dapat mengubah ikon aplikasi yang anda gunakan sehingga tampilan aplikasi menjadi lebih menarik.

## Error Notes

Pada project yang diperiksa terjadi sebuah error saat menjalankan aplikasi yakni terjadi force close akibat api key yang belum terisi pada file build.gradle.kts dan Saya mengatasinya dengan cara menambahkan api key yang valid

## Code Review

```kotlin
implementation("androidx.core:core-ktx:1.9.0")
implementation("com.google.android.material:material:1.9.0")
```

> Selalu gunakan versi terbaru dari Kotlin Plugin agar kode yang Anda tuliskan sesuai dengan best practice yang disarankan. Silahkan update pada file **build.gradle** level module.
> 

```kotlin
binding.tvGithubUser.text = "No account with that username"
```

> Penggunaan Hardcoded String sebaiknya dihindari, gunakan Android Resource String sesuai dengan best practice yang disarankan sehingga apabila nantinya aplikasi akan menggunakan fitur translate, teks tersebut dapat dengan mudah di ubah ke bahasa lain.
> 

```kotlin
fun saveThemeSetting(isDarkModeActive: Boolean) {
        viewModelScope.launch {
            pref.saveThemeSetting(isDarkModeActive)
        }
    }
```

> Kode yang tidak pernah digunakan baik itu Class, method, ataupun variable jika tidak digunakan sebaiknya dihapus. Kamu bisa memanfaatkan **Analyze - Code Cleanup** untuk melakukannya dengan cepat. Seperti contoh di atas method atau fungsi saveThemeSetting pada MainViewModel tidak pernah digunakan sehingga sebaiknya kode tersebut dihapus.
> 

![WhatsApp Image 2024-05-05 at 14.00.38_79f329cd.jpg](Technical%20Exercise%20Result%20(Android%204)%2047d02901c67c40708f82e509f48b4285/WhatsApp_Image_2024-05-05_at_14.00.38_79f329cd.jpg)

> Pada Halaman Detail daftar Following dan Follower tidak muncul saat orientasi diubah menjadi landscape. Anda dapat menggunakan Scroll View Layout pada halaman detail untuk menampilkan informasi dengan baik saat orientasi diubah menjadi landscape.
> 

![WhatsApp Image 2024-05-05 at 14.00.39_48afde80.jpg](Technical%20Exercise%20Result%20(Android%204)%2047d02901c67c40708f82e509f48b4285/903e2df5-b96c-4456-a4b3-314902de2331.png)

> Tampilan jumlah follower masih terpotong, sesuaikan ukuran Text View yang digunakan sehingga jumlah following dapat terlihat dengan jelas.
>