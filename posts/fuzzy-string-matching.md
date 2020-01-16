<!--
.. title: Fuzzy String Matching
.. slug: fuzzy-string-matching
.. date: 2020-01-16 6:00:00 UTC-05:00
.. tags: 
.. category: data-science 
.. link: 
.. description: Use fuzzy string matching algorithms to match ChiPy meetup and given names.
.. type: text
-->

## Overview

Data collection has and is rapidly expanding. However, data often isn’t submitted and/or collected without the required cleanliness or detail. At ChiPy we face the issue of trying to match Project Night attendees’ Meetup names with their legal names, which are needed for venue security. As a human it’s often easy to tell when names with slight variations match (Mike vs Michael; missing initials, etc), but trying to match hundreds of names one at a time is time consuming. Your job is to match the meetup and given names as accurately as possible using the fuzzy matching technique(s) of your choosing.

Background reading:  
- [The Name Matching You Need: A Comparison of Name Matching Technologies](http://www.basistech.com/whitepapers/the-name-matching-you-need-EN.pdf)  
- [An Ensemble Approach to Large-Scale Fuzzy Name Matching](https://medium.com/bcggamma/an-ensemble-approach-to-large-scale-fuzzy-name-matching-b3e3fa124e3c)  
- [Fuzzy Matching at Scale](https://towardsdatascience.com/fuzzy-matching-at-scale-84f2bfd0c536)  

Some Python libraries you might want to use:  
- [fuzzywuzzy](https://pypi.org/project/fuzzywuzzy/)  
- [textdistance](https://pypi.org/project/textdistance/)  
- [string_grouper](https://github.com/Bergvca/string_grouper)  


## Setup

There is no existing repo for this project, and no requirements to install. All you need to start is the data, which can be downloaded [here](https://drive.google.com/file/d/1WtW89K43Rwxq5ZM8Dyryv5EQgkkauOCF/view?usp=sharing).

Feel free to work how you see fit. That said, we strongly recommend setting up a virtual environment.

If you are using Linux or OS X, run the following to create a new virtualenv:

	python3 -m venv venv
	source venv/bin/activate
	pip install -r requirements.txt

On Windows, instead run the following:

	python3 -m venv venv
	venv\Scripts\activate
	pip install -r requirements.txt


## So what should we do?

The dataset has three columns: 
- meetup_id: The unique Meetup identifier for each user.  
- meetup_name: The publicly available display name of the Meetup user.  
- given_names: The "actual" name of the attendee, as given as a form response via Meetup.  

Each row in the dataset has the True matching name. In some cases, the meetup and given names match exactly, in some cases they don't. You won't need the meetup_id while actually attempting to match meetup and given names, but you can use it to validate your approach.

Some things you might want to consider along the way:

1. Are all the names usable? Could a human uniquely identify matches?
2. What patterns can be identified in the data we're working with?
3. What is our true goal with matching? In other words, when evaluating our process' success, how do we balance ensuring someone has preregistered with not turning too many people away at the door? To that end, what's the right evaluation metric to choose?
4. How might our approach differ if instead of a couple hundred names we have 10,000, a million, or even a billion names to match?


## Hints (for if you're stuck)
One easy way to load the data is with pandas:

```
	import pandas as pd

	read_kwargs = {
	    "header": 0,
	    "index_col": 0,
	    "skip_blank_lines": False,
	    "names": ["meetup_names", "given_names"]
	}

	data = pd.read_csv("fuzzy_names.csv", **read_kwargs).dropna()
	given_names = data["given_names"]
	meetup_names = data["meetup_names"]
```

The Levenshtein algorithm is one of the more basic and popular algorithms for fuzzy string matching. It has a few useful Python implementations, but fuzzywuzzy is probably the most popular.

Sklearn has modules dedicated to evaluation metrics. One very simple metric to evaluate how your matching is going is accuracy. Try starting with `from sklearn.metrics import accuracy_score`.


Happy Developing!
