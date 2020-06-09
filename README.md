Creating the new directory in HDFS:
    hdfs dfs -mkdir user/hadoop

Copying files from Local to HDFS:
  
    hdfs dfs -copyFromLocal Desktop/BDP/shakespeare.txt /user/hadoop/.
    hdfs dfs -copyFromLocal Desktop/BDP/word_list.txt /user/hadoop/.
    
Appending the file:
    hdfs dfs -appendToFile Desktop/BDP/word_list.txt /user/hadoop/shakespeare.txt
   
Creating new file and merging all the datasets:
    hdfs dfs -cat /user/hadoop/* | hdfs dfs -put -/user/hadoop/output.txt
