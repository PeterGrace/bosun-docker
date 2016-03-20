I want to try bosun, how do I do that?
======================================
  1. Make a local directory to save your hbase, scollector and bosun state via `mkdir -p ~/bosun ~/hbase`
  2. execute my opentsdb container via `docker run -v ~/hbase:/data/hbase --name=opentsdb -d -p 16010:16010 -p 4242:4242 petergrace/opentsdb-docker:latest`
  3. execute my bosun container via `docker run -v ~/bosun:/opt/bosun/data -d -p 8070:8070 --link opentsdb:tsdb petergrace/bosun-docker:latest`

