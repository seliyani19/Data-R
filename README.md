# Data-R
1. totalbidan_opendata
Data bidan di Jawa Barat berdasarkan kota/kabupaten, di akses di https://opendata.jabarprov.go.id/id/dataset/jumlah-tenaga-kebidanan-berdasarkan-kabupatenkota-di-jawa-barat pada tanggal 20-4-2022 jam 20:30 WIB

#import data total bidan di Jabar
library(readr)
totalbidan_opendata <- read_csv("https://raw.githubusercontent.com/seliyani19/Data-R/main/totalbidan-opendata.csv")

#Mengubah long format-wide format
bd_opendata = spread(totalbidan_opendata,tahun,jumlah_bidan)

#subsetting observations
#with operator >, <, >=, <=, ==, !=,
#memilih berdasarkan range urutan observasi/baris data bidan tahun 2020
bd_2020 = slice(totalbidan_opendata, 109:135)

names(bd_2020)
glimpse(bd_2020)
str(bd_2020)
summary(bd_2020)

names(bd_opendata)
glimpse(bd_opendata)
str(bd_opendata)
summary(bd_opendata)

names(totalbidan_opendata)
glimpse(totalbidan_opendata)
str(totalbidan_opendata)
summary(totalbidan_opendata)
