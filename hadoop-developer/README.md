# HADOOP-DEVELOPER LAB NOTES

<h3>Access HDFS in Terminal</h3> 
Dependencies: "lanier"<br>
Data: "html_site" "calllogs"<br>
Prerequisite: -<br>

<h3>Basic Spark-Shell</h3>
Dependencies: "nasdaq" <br>
Data: "NYSE_daily_prices_A.csv" "NYSE_daily_prices_B.csv" "NYSE_daily_prices_C.csv" "NYSE_daily_prices_F.csv" "NYSE_dividends_A.csv" "NYSE_dividends_B.csv" "NYSE_dividends_C.csv"<br>
Prerequisite: -<br>

<h3>Bloom Filters</h3>
Dependencies: "bloomfilter.jar" "filters" "dividendfilter" "bloomoutput"<br>
Data: "bloom_filters" NYSE_daily_prices_C.csv"<br>
Prerequisite: -<br>

<h3>Calculating Word Co-Occurances</h3>
Dependencies: "wordco.jar"<br>
Data: "word_co-occurrence" "writables"<br>
Prerequisite: "shakespeare"<br>

<h3>Collect Web Server Logs with Flume</h3>
Dependencies: "weblog" "weblogs_spooldir" <br>
Data: "flume"<br>
Prerequisite: -<br>

<h3>Create Populate Table Hive</h3>
Dependencies: -<br>
Data: "device":MySQL "webpage":MySQL<br>
Prerequisite: "lanier"<br>

<h3>Creating Inverted Index</h3>
Dependencies: "invertedindex.jar" "invertedIndexInput"<br>
Data: "inverted_index" "invertedIndexInput.tgz"<br>
Prerequisite: -<br>

<h3>Explore RDDs with Spark-Shell</h3>
Dependencies: "iplist"<br>
Data: "frostroad.txt"<br>
Prerequisite: "weblog" "access_log" <br>

<h3>Getting Started</h3>
Dependencies: -<br>
Data: -<br>
Prerequisite: -<br>

<h3>HBase as Data Warehouse</h3>
Dependencies: "hbase_lab"<br>
Data: -<br>
Prerequisite: -<br>

<h3>How Intergrated HBase Hive</h3>
Dependencies: -<br>
Data: -<br>
Prerequisite: -<br>

<h3>Implementing Custom WritableComparable</h3> 
Dependencies: "stringpairtest.jar"<br>
Data: "writables" "nameyeartestdata"<br>
Prerequisite: -<br>

<h3>Import MySQL Data Using Sqoop</h3>
Dependencies: "accounts" "webpage"<br>
Data: "sqoop" "accounts":MySQL "webpage":MySQL "lanier":MySQL<br>
Prerequisite: - <br>

<h3>Importing Data with Sqoop</h3>
Dependencies: "movierating" "movie"<br>
Data: "movierating":MySQL "movie":MySQL "movielens":MySQL<br>
Prerequisite:<br>

<h3>InputFormat</h3>
Dependencies: "movingaverage.jar" "stocks"<br>
Data: "moving_average" "NYSE_daily_prices_F.csv"<br>
Prerequisite: "closingprices"<br>

<h3>Joining Data Set in Hive</h3>
Dependencies: -<br>
Data: "hive" "NYSE_daily_prices_F.csv" "NYSE_dividends_F.csv"<br>
Prerequisite: "hive_data" "dividends_F.csv" "prices_F.csv"<br>

<h3>Logging</h3>
Dependencies: "logging.jar" "toolrunner.jar" "outdir"<br>
Data: "logging"<br>
Prerequisite: "shakespeare"<br>

<h3>Manipulating Data with Hive</h3>
Dependencies:<br>
Data: "hive"<br>
Prerequisite: "movie" "movierating"<br>

<h3>MapReduce Joins</h3>
Dependencies: "mapside.jar" "mapsidejoin.jar" "stocks" "joinoutput"<br>
Data: "map_join" "NYSE_dividends_A_join.csv" "NYSE_daily_prices_A.csv"<br>
Prerequisite: -<br>

<h3>More Pratice with MapReduce Java Programs</h3>
Dependencies: "processlog.jar" <br>
Data: "log_file_analysis"<br>
Prerequisite: "weblog" "testlog"<br>

<h3>OutputFormat</h3>
Dependencies: "dividend.jar" "growth" "DividendJob_0" "DividendJob_1" "DividendJob_2"<br>
Data: "custom_sorting"<br>
Prerequisite: -<br>

<h3>Partition Data with Hive</h3>
Dependencies: -<br>
Data: -<br>
Prerequisite: "lanier" "accounts_avro"<br>

<h3>Pig Intro</h3>
Dependencies: -<br>
Data: "pig_intro" "student.txt"<br>
Prerequisite: -<br>

<h3>Pig Use Case: Baseball Stats</h3>
Dependencies: "baseball" "input"<br>
Data: "Batting.csv" "Master.csv"<br>
Prerequisite: -<br>

<h3>Pratice Selecting Data in Hive</h3>
Dependencies: "hive_data" "prices_F.csv" "dividends_F.csv" "prices_f" "stock_f"<br>
Data: "hive" "NYSE_daily_prices_F.csv" "NYSE_dividends_F.csv"<br>
Prerequisite: -<br>

<h3>Run Yarn Job and Observe</h3>
Dependencies: -<br>
Data: -<br>
Prerequisite: "lanier" "html_site" <br>

<h3>Running MapReduce Job</h3>
Dependencies: "wordcounts" "wc.jar" "pwords" "count2"<br>
Data: -<br>
Prerequisite: "shakespeare"<br>

<h3>Running Oozie Workflow</h3>
Dependencies: -<br>
Data: "oozie-labs"<br>
Prerequisite: -<br>

<h3>Store Access Data in non-Text Format</h3> 
Dependencies: -<br>
Data: "data-format" "accounts":MySQL "lanier":MySQL<br>
Prerequisite: "lanier" "accounts_avro"<br>

<h3>UDFS in Pig</h3>
Dependencies: "stockudfs.jar" "stockvolume.pig"<br>
Data: "pig_udfs" "NYSE_daily_prices_A.cvs"<br>
Prerequisite: -<br>

<h3>Using Combiner</h3>
Dependencies: "combiner.jar"<br>
Data: "combiner"<br>
Prerequisite: "wordcount"<br>

<h3>Using Counters and Map-Only Job</h3>
Dependencies: "counters.jar"<br>
Data: "counters"<br>
Prerequisite: "weblog" "testlog"<br>

<h3>Using HDFS</h3>
Dependencies: "shakespeare" "weblog" "testlog" "access_log" "test_access_log" "shakepoems.txt"<br>
Data: "shakespeare.tar.gz" "access_log.gz" <br>
Prerequisite: -<br>

<h3>Using Squencefiles File Compression</h3>
Dependencies: "readsequencefile.jar" "createsequencefile.jar" "uncompressedsf" "uncompressedsf" "compressedsftotext" "sequence.jar" <br>
Data: "createsequencefile" <br>
Prerequisite: "access_log" "weblog" <br>

<h3>Using ToolRunner and Passing Parameters</h3>
Dependencies: "toolrunnerout" "toolrunner.jar"<br>
Data: "toolrunner" <br>
Prerequisite: "shakespeare"<br>
IMPORTANT NOTE: This Lab must be taught after "Writing a MapReduce Java Program" due to instructional requirements

<h3>Writing MapReduce Jave Program</h3>
Dependencies: "avgwordlength.jar" "wordlengths" <br>
Data: "averagewordlength" <br>
Prerequisite: "shakespeare" <br>

<h3>Writing MapReduce Streaming Program</h3>
Dependencies: "avgwordstreaming" <br>
Data: "averagewordlength" <br>
Prerequisite: "shakespeare" <br>

<h3>Writing Partitioner</h3> 
Dependencies: "partitioner.jar" <br>
Data: "partitioner" <br>
Prerequisite: "weblog" "testlog" <br>

<h3>Writing Unit Tests with MRUnit Framework</h3>
Dependencies: - <br>
Data: "mrunit" <br>
Prerequisite: - <br>