# Spark-Infra

 Checkout the project, copy the jar and csv to apps and data folder and then run

 docker compose up -d
 docker ps
 docker logs -f spark-infra-spark-master-1 --tail 100

 Open another terminal and run

 docker exec -i -t spark-infra-spark-master-1  /bin/bash
 cd bin/
 ./spark-submit --master spark://0.0.0.0:7077 --name read-write --class com.nuwas.ReadAndWriteCSV  local:///opt/spark-apps/spark_scala_2.12-0.1.0-SNAPSHOT.jar /opt/spark-data/data.csv /opt/spark-data/parquet

Screenshot 

![WhatsApp Image 2024-09-30 at 8 55 21 AM](https://github.com/user-attachments/assets/b13036e3-ee9b-426d-8053-27706278f911)
