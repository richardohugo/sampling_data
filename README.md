step code





git init
add .
git commit -m "initial commit"
git log

#import data
wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx
--2022-04-30 11:20:26--  https://github.com/labusiam/dataset/raw/main/weather_data.xlsx
mv weather_data.xlsx ~
ls

#operasi data
in2csv -n weather_data.xlsx #info jumlah sheet
in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv #ambil sheet weather 2014 jadikan file terpisah .csv
in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv #ambil sheet weather 2015 jadikan file terpisah .csv
cat weather_2014.csv weather_2015.csv > weather_data.csv #gabung 2 csv file data jadi 1
rm weather_data.xlsx #hapus file xlsx
csvlook weather_data.csv | sample -r 30% > sample_weather.csv #huntuk ambil sample sebesar 0.3
ls #cek file
