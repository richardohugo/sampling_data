# sampling_data

#script sampling.sh


wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx #untuk download file xlsx
mv weather_data.xlsx ~ #memindahkan ke direktori lokal

in2csv -n weather_data.xlsx #info jumlah sheet
in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv #convert sheet weather_2014 ke weather_2014.csv
in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv #convert sheet weather_2015 ke weather_2015.csv
cat weather_2014.csv weather_2015.csv > weather_data.csv #menggabungkan kedua data csv menjadi weather_data.csv
rm weather_data.xlsx #hapus weather_data.xlsx
csvlook weather_data.csv | sample -r 30% > sample_weather.csv #ambil sample sebanyak 30% dari data pada weather_data.csv kemudian dijadikan file terpisah sample.csv
