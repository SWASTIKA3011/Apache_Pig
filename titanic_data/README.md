## Titanic Dataset Analysis
This repository contains a Pig script that analyzes the Titanic dataset to determine various statistics, including the number of passengers, number of survivors, and the count of female and male passengers and survivors.

### Dataset
The dataset used for this analysis is the Titanic dataset, which contains information about the passengers aboard the Titanic. The dataset includes details such as Name, Passenger Class, Age, Sex, Suvived, Sex Code.

### Requirements
To run the Pig script, you will need:
Apache Pig installed on your system.
The Titanic dataset in a suitable format (e.g., CSV) and accessible from the Pig script.

### Usage
Follow these steps to run the Pig script and perform the analysis:
- Ensure that you have Apache Pig installed on your system. If not, refer to the official Apache Pig documentation for installation instructions.
- Place the Titanic dataset file in a location accessible from the Pig script.
- Open the Pig script file, titanic.pig, and modify the following line:
    __"titanic_data = LOAD 'path/to/titanic_dataset.csv' USING PigStorage(',') AS (...);"__.
    Replace 'path/to/titanic_dataset.csv' with the actual path to the Titanic dataset file.
- Review the Pig script to understand the analysis logic and modify it if necessary.
- Run the Pig script using the following command:
       __"pig -x local titanic_analysis.pig"__. 
       This command executes the Pig script in local mode(You can also run with HDFS).
- Once the script finishes executing, it will output the following statistics:
    - Number of passengers: [value]
    - Number of survivors: [value]
    - Number of female passengers: [value]
       * Number of male passengers: [value]
       * Number of female survivors: [value]
       * Number of male survivors: [value]

### Note
- The Pig script assumes that the dataset is in a comma-separated values (CSV) format. Modify the LOAD statement accordingly if your dataset is in a different format.
- Make sure that the dataset file is properly formatted and contains the required fields for analysis (e.g., 'sex', 'survived', etc.).
- If your dataset has different column names or structure, adjust the Pig script accordingly to match your dataset's schema.

Feel free to modify the Pig script or extend the analysis as per your requirements and dataset characteristics.
