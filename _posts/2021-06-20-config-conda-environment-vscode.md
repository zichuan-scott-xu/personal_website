---
layout: post
title:  "How to config conda environment in VSCode Python extension?"
date:   2021-06-20 10:00:00
blurb: "A look at an example post using Bay Jekyll theme."
---

The Python extension of VSCode may not be able to find the conda extension and especially, its virtual environment. 
As a frantic of VSCode, I've struggled a while to configurate the extension and hope that the following suggestions are 
helpful. 

First, click the gear-like button in the left lower corner of the VSCode to open up the setting page. Enter 'python' 
and click 'edit in settings.json'. This will open the configuration file for Python extension in VSCode. 

Here's the **most important step**: add the following lines inside the outermost curly brackets: 
```json
    "python.experiments.enabled": true,
    "python.experiments.optInto": [
        "pythonDiscoveryModule"
    ]
```

Restart the VSCode and you should see virtual environments also appearing in the list where you used to select Python environment.  

In this configuration file, you can also change the `python.defaultInterpreterPath` if needed to set a default python executable every time you 
open VSCode. 