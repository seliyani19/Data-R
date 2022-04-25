# Data-R
1. totalbidan_opendata
Data bidan di Jawa Barat berdasarkan kota/kabupaten, di akses di https://opendata.jabarprov.go.id/id/dataset/jumlah-tenaga-kebidanan-berdasarkan-kabupatenkota-di-jawa-barat pada tanggal 20-4-2022 jam 20:30 WIB

#import data total bidan di Jabar
library(readr)
totalbidan_opendata <- read_csv("https://raw.githubusercontent.com/seliyani19/Data-R/main/totalbidan-opendata.csv")

#Mengubah long format-wide format
bd_opendata = spread(totalbidan_opendata,tahun,jumlah_bidan)
