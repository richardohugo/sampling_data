# script.sh



in2csv weather_data.xlsx > weather_data.csv
~$ git init
~$ add .
~$ git commit -m "initial commit"
~$ git log
$ wget https://github.com/labusiam/dataset/raw/main/weather_data.xlsx

~$ mv weather_data.xlsx ~
~$ ls

~$ in2csv -n weather_data.xlsx
~$ in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv
~$ in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv
~$cat weather_2014.csv weather_2015.csv > weather_data.csv
~$ rm weather_data.xlsx
:~$ cat weather_data.csv | sample -r 0.3 | head > sample_weather.csv
~$ ls
