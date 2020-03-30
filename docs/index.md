Saya memiliki koleksi dataset dan bermaksud untuk membagikannya kepada teman-teman.

## Unduh data

Dataset ini dapat teman-teman unduh dalam format `csv` dan `rds`. Metadata sederhananya dalam berkas `txt`.

Untuk sementara teman-teman dapat mengaksesnya dari [repositori github](https://github.com/akherlan/dataset) saya. Ke depan, saya ingin buatkan daftar, penjelasan dataset, disertai tautan unduhnya. Semoga.

## Mengakses dataset menggunakan R

Teman-teman juga bisa mengakses dataset ini langsung dari RStudio menggunakan library pins. Konfigurasi pertamanya bisa teman-teman ikuti [disini](http://pins.rstudio.com/articles/boards-github.html).

```{r}
# memuat/menginstal library yang dibutuhkan
if (!require("pins")) install.packages("pins")

# membuat koneksi ke dataset dengan nama "databoard"
board_register(name ="databoard", repo = "akherlan/dataset", board = "github")

# mencari dataset dengan kata kunci "eartquake"
pin_find(text = "eartquake", board = "databoard")

# menggunakan dataset
gempa <- pin_get("quake", board = "databoard")
```
Terima kasih.

-----

<center>Hosted on <a href='https://github.com/akherlan/dataset'>gihub page</a>.</center>
