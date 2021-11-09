 # Answers
 ## Exercise 1
 QN 1. creating project directory
```
mkdir Exercise
```
QN 2. creating directories for a bioinformatics project
```
cd Exercise
mkdir Bioinfo_project
cd Bioinfo_project/
mkdir Documents Data Scripts
cd Data/
mkdir Raw_data Processed_data
```
QN 3. downloading a fasta file
```
cd Raw_data
wget https://raw.githubusercontent.com/kipkurui/IntroductoryLinux/master/Data/nrf1_seq.fa
cp nrf1_seq.fa ../Processed_data/nrfi_seq_copy.fa
```
QN 4.
```
cd ../Processed_data
grep '^>' nrfi_seq_copy.fa >sequence_names.txt
```
QN 5 Script file for QN 4.
```
cd ../../../Bioinfo_project/Scripts/
nano extract_seq.sh
```
- type into the editor the following 
```
#!/usr/bin/env bash

#Ascript for extracting the sequence headers in a fasta file


grep "^>" ../../Bioinfo_project/Data/Processed_data/nrfi_seq_copy.fa > sequence_names.txt

#move the file to processed data
mv sequence_names.txt ../Data/Processed_data
```
- add execution rights to the file by running the following command
```
chmod +x extract_seq.sh
```
- Run extract_seq.sh file using the command bellow
```
./extract_seq.sh
```



- Click [here](https://github.com/ndugwa/intro_github/blob/main/henry.sh) to go extract_seq.sh
