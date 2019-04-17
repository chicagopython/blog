<!--
.. title: ChiPy Chipmunk Project Night 
.. slug: chipy-chipmunks
.. date: 2019-04-18 18:00:00 UTC-05:00
.. tags: pandas, statistics, EDA, analytics
.. category: data-science 
.. link: 
.. description: Explore questions surrounding the amazing ChiPy chipmunks. 
.. type: text
-->

## Project Night Purpose

Many people assume data scientists spend all day visualizing data and making impressive predictive models. While this isn’t untrue, the luckiest and most productive data scientists spend a lot of their time communicating. They communicate their model results - as well as their assumptions and limitations when making their models and doing analysis - in a way that is digestible to their stakeholders and colleagues. 

Tonight’s project is aimed towards that aspect of communication. You will be asked to make assumptions as a team - particularly as they pertain to this problem and what the stakeholders need. There are no exactly correct assumptions or answers for this project night. There may be assumptions and answers that clearly don’t have evidence to support them, but do not feel bogged down by getting the “right” answer.

Most importantly - have fun. While this project night covers serious concepts, it is ridiculously silly and meant to be taken with a bit of lighthearted exploration and plenty of opportunities to make mistakes.

## Setting up your environment
 
This project is contained in a jupyter notebook and is assuming you have Python 3.+ installed on your machine. If this is your fisrt project night, we recommend creating a folder for the project night repo: `mkdir chipy_projects && cd chipy_projects`. If you already have the project night repository on your machine, go to that directory and pull from master.

If you are using Linux or OS X, run the following to create a new virtualenv:

```
python3 -m venv chipmunk
source chipmunk/bin/activate
```

On Windows, run the following

```
python3 -m venv chipmunk 
chipmunk\Scripts\activate
```

## Getting the project
The project is in the ChiPy project night repo. If you do not have the repository already, run 
```
git clone https://github.com/chicagopython/CodingWorkshops.git
``` 

Now we will:

Go to the project:
```
cd CodingWorkshops/problems/data_science/chipmunks
```

Install the packages we need into our environment:
```
pip install -r requirements.txt
```

Run our jupyter notebook server for the project:
```
jupyter notebook
```

## Have fun!
