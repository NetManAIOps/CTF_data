# CTF_dataset
CTF_dataset is the dataset for the paper "CTF: Anomaly Detection in High-Dimensional Time Series with Coarse-to-Fine Model Transfer"

## Data

### Dataset Information

| Dataset name|number of machine entities | metric number |
|:------------:|:----------:|:-----:|
| CTF_dataset | 533 | 49 |
| **number of training time points <br> in each machine** | **number of test time points <br> in each machine** | |
|  5 * 2880 | 8 * 2880 | |

### Clone the repo and unzip the folder

```
git clone https://github.com/smallcowbaby/CTF_data && cd CTF_data && cat CTF_data.tar.gz.* | tar -zxv
```


### CTF_dataset

CTF_dataset is collected from a top global Internet company, where geo-distributed data centers serve global users. The businesses running on the infrastructure are typical Internet services (e.g., news, advertisement, videos).
It contains 533 machine entities, and each is monitored with 49 KPIs. 
KPIs are collected every 30s spanning 13 days (from April 18th to April 30th). 
In the experiment, we use the first five days’ data for training and the latter eight days’ data for testing.


Thus DOMI_dataset is made up by the following parts:

* `CTF_data.tar.gz.**/`: Monitoring data. After unzipping the folder, each file contains the monitoring data of one machine one day. For each file, each line in the file is the 49 monitored metrics at one timestamp and there are 2880 lines.
* `label_result/`: The labels of the testing set, which indicate whether each time point of each machine is an outlier. It contains 533 files, each of which corresponds to one machine entity. For each file, it contains 23040 (8 * 2880 time points) 0/1 labels.
