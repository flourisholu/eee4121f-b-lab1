# eee4121f-b Lab 1

This README includes the steps needed to run the tcp.py experiments.

## Installation

Install the python statistics module
```
sudo apt-get install update
sudo apt-get install python-statistics
```
## Viewing images
The plot graph is saved as **rtt.png** and the queue graph is saved as **queue.png**. You can use `fim rrt.png` and `fim queue.png` to view the RTT and queue plots, respectively.

## Running TCP experiments
There are three experiments run for each TCP algorithm. For each experiment, changes are made in the *run.sh* bash script. Changes are made to this section of code:
```python
# You can change these parameters:
bwhost=1000
qsize=100
cong=cubic
```
### TCP Reno
1. Experiment 1: No changes need to be made
2. Experiment 2: Change `qsize` to 20
3. Experiment 3: Change `bwhost` to 100 and `qsize` to 100

### TCP Cubic
1. Experiment 1: Uncomment `--cong=$cong \` under the comment `#Now start the experiment and load the parameters` and change `bwhost` back to 1000
2. Experiment 2: Change `qsize` to 20
3. Experiment 3: Change `bwhost` to 100 and `qsize` to 100

### TCP BBR
1. Experiment 1: Uncomment `--qman=$qman \` under the comment `#Now start the experiment and load the parameters`, make `cong=bbr`, and change `bwhost` back to 1000
2. Experiment 2: Change `qsize` to 20
3. Experiment 3: Change `bwhost` to 100 and `qsize` to 100
