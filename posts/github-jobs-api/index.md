<!--
.. title: GitHub Jobs API
.. slug: github-jobs-api
.. date: 2019-04-15 18:00:00 UTC-05:00
.. tags: api, EDA
.. category: data-science 
.. link: 
.. description: Use the GitHub jobs API to explore open job postings.
.. type: text
-->

## Project Night Purpose

All of us need to look for a job at some point; and most every job board has its own API for users to post and pull data (though usually they charge money for access). The [GitHub Jobs page](https://jobs.github.com) is a great simple API for a first look at this kind of data acqusition and analysis.

Tonight's project uses the very popular Python HTTP library [requests](https://2.python-requests.org/en/master/) along with [json](https://docs.python.org/3/library/json.html) from the standard library. You will explore the data in the jobs API with the intent of learning something about the current job market for devs. There are a ton of caveats here: for example,

* Who chooses to post to GitHub Jobs? Are they representative of the overall population?
* How old are the postings?
* Is it safe to extrapolate statistics to the country? to Illinois? to Chicago?

Although the topic is a little serious we want to make sure you don't get discouraged by the data you pull (ask around--how many people in your group got their job from a GitHub posting?). The GitHub site shouldn't be taken as a good primary source for job availability or category...but that's part of data acquistition and analysis: assessing the strenghts and shortcomings of your data source. Possible discusison points for the group are things like:

* Where might you get additional information?
* How often should you pull the data? What would capture over time give you?
* Does the dataset tell you anything about which companies use the GitHub for hiring at all? In which cities? Should we move to a different part of the country?
* Choose your own adventure and share with the group what you have learned!


Most importantly - have fun! Accessing an API is a great core skill for data analysis and all experience is good experience. We hope that you are creative in your explanation and that each group discovers different things!


## Setting up your environment

There is no pre-written code for this project, but we assume you have Python 3.+ installed on your machine.  If this is your fisrt project night, we recommend creating a folder for the project night repo: `mkdir chipy_projects && cd chipy_projects`. If you already have the project night repository on your machine, go to that directory and pull from master.

If you are using Linux or OS X, run the following to create a new virtualenv:

```
python3 -m venv github_jobs_api
source github_jobs_api/bin/activate
```

On Windows, run the following

```
python3 -m venv github_jobs_api 
github_jobs_api\Scripts\activate
```

## Getting the project
The project is in the ChiPy project night repo. If you do not have the repository already, run 
```
git clone https://github.com/chicagopython/CodingWorkshops.git
``` 

Now we will:

Go to the project:
```
cd CodingWorkshops/problems/data_science/github_jobs_api
```

Install the packages we need into our environment:
```
pip install -r requirements.txt
```

view the _README.md_ file for additional information:
```
cat README.md
```

## Have fun!
