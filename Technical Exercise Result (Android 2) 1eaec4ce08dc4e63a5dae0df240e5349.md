# Technical Exercise Result (Android 2)

### Project name: Submission MyStoryApp

## Project Summary

- Tampilan Google Maps masih belum muncul pada halaman Story Locations, silakan cek penggunaan Google Maps Android API v2 pada aplikasi yang anda buat.
- Penggunaan import dan safe call yang tidak diperlukan sebaiknya dihapus. Kamu bisa memanfaatkan fitur Problems > File untuk mengecek semua warning terkait penggunaan kode yang tidak diperlukan pada file terkait
- Sebaiknya gunakan versi terbaru dari setiap dependensi dan plugin yang digunakan sesuai dengan best practice yang disarankan
- Hindari penggunaan Hardcoded String, anda dapat manfaatkan Android String Resource.
- Perhatikan penggunaan layout dan desain tampilan yang digunakan sehingga tidak mengganggu experience pengguna saat menggunakan aplikasi anda.

## Code Review

![WhatsApp Image 2024-05-05 at 18.34.28_a0cc358b.jpg](Technical%20Exercise%20Result%20(Android%202)%201eaec4ce08dc4e63a5dae0df240e5349/WhatsApp_Image_2024-05-05_at_18.34.28_a0cc358b.jpg)

> Pada Halaman Story Locations, tampilan google maps belum muncul. Silakan cek penggunaan Google Maps Android API v2 yang anda pakai apakah sudah sesuai atau belum. Jika sudah sesuai silakan cek apakah Google Maps Android API v2 yang anda gunakan sudah diaktifkan (enabled) atau belum.
> 

![WhatsApp Image 2024-05-06 at 14.53.15_4fa8d82f.jpg](Technical%20Exercise%20Result%20(Android%202)%201eaec4ce08dc4e63a5dae0df240e5349/WhatsApp_Image_2024-05-06_at_14.53.15_4fa8d82f.jpg)

> Pada Halaman Setting layout halaman masih terpotong saat orientasi diubah menjadi landscape. Anda dapat menggunakan Scroll View Layout pada halaman Setting agar dapat menampilkan informasi dengan baik saat orientasi diubah menjadi landscape.
> 

```kotlin
implementation("androidx.core:core-ktx:1.10.1")
...
implementation("com.google.android.material:material:1.9.0")
...
```

> Selalu gunakan versi terbaru dari Kotlin Plugin dan dependensi yang anda gunakan agar kode yang Anda tuliskan sesuai dengan best practice yang disarankan. Silahkan update versi plugin dan dependensi yang anda gunakan pada file **build.gradle**.
> 

```kotlin
android:text="Share Location"
```

> Penggunaan Hardcoded String sebaiknya dihindari, gunakan Android Resource String sesuai dengan best practice yang disarankan. Dengan demikian aplikasi dapat menggunakan fitur translate dengan lebih mudah untuk mengubah teks tersebut ke bahasa lain.
> 

```kotlin
...
import android.provider.Settings.Global.getString
...

inner class ListViewHolder(private var binding: ItemRowStoryBinding) :
        ...
                if(storyItem?.createdAt != null) {
                    val datePosted = DateFormatter.formatDate(storyItem?.createdAt.toString(), TimeZone.getDefault().id)
                    ...
                }
        ...
    }
```

> Penggunaan import dan safe call yang tidak diperlukan sebaiknya dihapus. Kamu bisa memanfaatkan fitur Problems > File untuk mengecek semua warning terkait penggunaan kode yang tidak diperlukan pada file terkait
>