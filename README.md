# MapReduce_Ubuntu

..........................................................
# MapReduce

Downloads Folder- (copy and paste in URL)

https://drive.google.com/drive/folders/1JGOAnuABVAmLRcw0hdccbx1djcjpMAre?usp=sharing

CMD - 

1.  mkdir MapReduceTutorial111
  
  
   files(SalesCountryDriver,SalesCountryReducer,SalesJan2009,SalesMapper,Manifest.txt) have pasted in (MapReduceTutorial) directory..  with help of folder


.... given in description....



2. sudo chmod -R 777 MapReduceTutorial111

3. cd MapReduceTutorial111
4. hadoop version 
5. export CLASSPATH="$HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-client-core-3.3.5.jar:$HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-client-common-3.3.5.jar:$HADOOP_HOME/share/hadoop/common/hadoop-common-3.3.5.jar:~/MapReduceTutorial111/SalesCountry/:$HADOOP_HOME/lib/"


6. javac -d . SalesMapper.java SalesCountryReducer.java SalesCountryDriver.java 

7. sudo chmod -R 777 SalesCountry


8. jar cfm ProductSalePerCountry.jar Manifest.txt SalesCountry/*.class

9. hadoop fs -mkdir /inputMapReduce11

10. hadoop fs -copyFromLocal  SalesJan2009.csv  /inputMapReduce11
    NOTE - (please change the name and rollnumber)

11. hadoop jar ProductSalePerCountry.jar /inputMapReduce11 /mapreduce_output_sales11

12. hadoop fs -cat /mapreduce_output_sales11/part-00000
............................................................
