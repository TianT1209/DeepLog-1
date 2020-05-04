# DeepLog
This is the achievement of core DeepLog and it is a manual version not for industrial usage.

> For the dataset, I give some examples and you can put your own data into that folder.

**The Deeplog_demo is a relatively complete package, you can try to implement that.**

![workflow](https://github.com/Wapiti08/DeepLog/blob/master/Deeplog_demo/Pic/Deeplog_dataflow.png)

## Instructions
This is the instruction how to use the a series of modules to pre-process the raw system logs to key logs

## Statement:
The model is based on off-line work, we will achieve online real-time detection in the future

The following is the instructions on how to implement the whole module:
##  1. Source data:
When the data format is in csv, we need translate them into txt files.

##  2. Data analysis:
we use the logparser tool to transform the source txt log files into structured csvs under a folder, the folder is named by the start and end time
*(use Lenma_demo.py with python2)
In the stage, we calculate the EventTemplate for every log

##  3. Variable Selection:
The log_value_vector_1.py will be used to generate the csv file like Parameter_vector.png, which will be used to implement the anomaly detections later. (and has been integrated into models already)

##  4. Model detection:
Basiclly, we have two modules. 

- Whereas, before implementing the modules, we will first see whether there is obvious malicious logs, we will report them first.
	
- After that, we will first implement execution path anomaly detection with Execution_Path_Anomaly.py
	
- Finally, we will implement parameter values anomaly detection with Parameter_value_performance_anomaly.py	


If you want to implement the raw version, please execute:
pip install -r requirement.txt


## References：
*1.Execution Anomaly Detection in Distributed Systems through Unstructured Log Analysis*

*2.DeepLog: Anomaly Detection and Diagnosis from System Logs*
