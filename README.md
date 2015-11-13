#  This script generates the files needed by cluster simulator from google traces
#  as described in https://drive.google.com/file/d/0B5g07T_gRDg9Z0lsSTEtTWtpOW8/view
#  input 1: Google simulator job_events file (we assume that all csv files are concatenated in one file)
#  input 2: Google simulator task_events file (we assume that all csv files are concatenated in one file)
#  output 1: Debug file that prints all data from all jobs. Each row represents one job
#  Format: job_id | scheduling_class | submit_timestamp | schedule_timestamp | finish_timestamp
#   | aggregated_cpu (num cores) | aggregated_memory (in bytes, assumed 4gb RAM) | interarrival_time
#   | task_number
#  output 2: init-cluster-state file containing jobs that started before simulation time window as
#  described in https://github.com/google/cluster-scheduler-simulator/tree/master/traces
#  output 3: all-cluster-state file containing all jobs as in order to generate more realistic synthetic jobs
#  described in https://github.com/google/cluster-scheduler-simulator/tree/master/traces
#  output 4: csizes_cmb as described in https://github.com/google/cluster-scheduler-simulator/tree/master/traces/job-distribution-traces
#  output 5: runtimes_cmb as described in https://github.com/google/cluster-scheduler-simulator/tree/master/traces/job-distribution-traces
#  output 6: runtimes_cmb as described in https://github.com/google/cluster-scheduler-simulator/tree/master/traces/job-distribution-traces
