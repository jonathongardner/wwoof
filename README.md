# WWOOF
Data scraper for wwoofusa. This contains a ruby script to populate a `data.csv` file with information from wwoofusa.org.

## Iniital Setup
Install packages/gems (this only needs to be run once):
```bash
gem install typhoeus
gem install nokogiri
```

## Running
Create/add urls to `data.csv` with the following format:
```csv
url,
https://wwoofusa.org/user/5661,
https://wwoofusa.org/user/271283,
https://wwoofusa.org/user/27123,
```

From within this directory run:
```bash
./parse
```
HINT: To navigate to this directory open a terminal type `cd ` (space at the end it necessary) and drag the folder into the terminal (this should auto fill the directory path) hint enter.

NOTE: If `./parse` doesn't work you can try `ruby parse`

The `./parse` command will only parse data for urls that dont already have the first field (i.e. `review`) if you want to force it to rerun all urls do `RELOAD=SURE ./parse`.

## Adding more csv fields
