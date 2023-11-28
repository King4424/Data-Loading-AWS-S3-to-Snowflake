# :sun_behind_small_cloud: Data Loading AWS-S3 to Snowflake
Detailed Steps to Load Structured Data from External Source Like AWS S3 to Snowflake Database

### :snowflake: Load Market capitalization Report Dataset into Snowflake through Snowflake Dashbord
### The basic steps to load local data into snowflake:
1.Check the input source type of your Dataset.

2.Create AWS S3 Bucket and upload dataset file into it.

3.Create file format according to dataset on snowflake.

4.Create External Stage to connect AWS S3 to Snowflake. 

5.Create & Run target table SQL Command.

6.Select database, schema and table.

7.Load data into table through stage.

**After we have the source input, let us check the data first:**
<img width="939" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/f5ddd259-cbaa-4ed4-9c11-811ef32bdb5c">

:star2: We should notice that there is a redundant header in the first line we will not use it. Also, the data format needs to be processed carefully, as there is no second suffix. The comma in a inner sentence should be isolated, it is not a delimiter anymore. All these works need to be done before we load data to table of database.

:star2:  The next step is to create the File Format in Snowflake. We need to choose which one database and schema:
<img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/bdf1fc5e-3069-4313-a670-2a23da4ee37c">

We can see the File Format has been created on your selected Database and schema.
<img width="948" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/217ad701-8090-47d3-8618-b9a5068dfae8">

:star2:  Now we have to Create Stage to connect with AWS S3 Bucket:
<img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/b1628bc2-9018-4f16-ba3c-100f6fbcf32e">

 We can see the External Stage has been created and Dataset file is visible to us on your selected Database and schema.
 <img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/939adaaa-cfc5-48c3-9b8b-2e96ff743ee2">

 :star2: The next step is to create the target table to Snowflake. We need to choose which one database and schema we want to upload. The constraints can be roughly used:
<img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/419b31ef-d6d4-4b81-9fb9-d801e08abedf">

 :star2: Load Data into table through stage we created earlier and select File format, Header, Field delimiter, Field optionally enclosed by:
 <img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/de61ffa5-29eb-472e-9304-3473858f2cc7">

 <img width="952" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/52dbd95b-b3e1-4497-9841-6850e02d6cc4">

 :star2: See Data Preview:
 <img width="936" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/08b3d6cf-4433-4f09-9f18-24b7a60be32b">

:star2: We can also use sql queries to check data using < Select * from > :
<img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/866da341-f552-4d04-847a-4d773c96233e">

✅ That's All. We managed to load the data from the local to Snowflake.

📊 We can also do Analysis of our Data using snowflake charts and filters:
<img width="960" alt="image" src="https://github.com/King4424/Data_Loading-AWS-S3-to-Snowflake/assets/121480992/6e03bd9c-333b-4e4f-b66e-a22a10b1a1a9">







 
 


