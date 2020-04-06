# cloud-systems

## Steps

1. Download the Covid-19 data files for the specified date range

   `python DownloadCovid19Data.py dd-mm-yyyy dd-mm-yyyy`
   e.g. `python DownloadCovid19Data.py 01-22-2020 04-05-2020`

2. Prepare the Covid-19 data files into different directories depending on the format of the files.
 
   `python PrepareCovid19Data.py dd-mm-yyyy dd-mm-yyyy`
   e.g. `python PrepareCovid19Data.py 01-22-2020 04-05-2020`
  
3. Copy the prepared data from the local directory to HDFS

   hadoop fs -mkdir /prepared-data
   hadoop fs -put ../prepared-data/* /prepared-data
