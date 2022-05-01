<<<<<<< HEAD
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
=======
# sampling_data

#script sampling.sh
#editor --> untuk membuat script code
chmod +x sampling.sh #run script code

wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx #untuk download file xlsx
mv weather_data.xlsx ~ #memindahkan ke direktori lokal

in2csv -n weather_data.xlsx #info jumlah sheet
in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv #convert sheet weather_2014 ke weather_2014.csv
in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv #convert sheet weather_2015 ke weather_2015.csv
cat weather_2014.csv weather_2015.csv > weather_data.csv #menggabungkan kedua data csv menjadi weather_data.csv
rm weather_data.xlsx #hapus weather_data.xlsx
csvlook weather_data.csv | sample -r 30% > sample_weather.csv #ambil sample sebanyak 30% dari data pada weather_data.csv kemudian dijadikan file terpisah sample.csv
>>>>>>> dc25a134772c3070cfe88b26c68b19a02da0ed07
