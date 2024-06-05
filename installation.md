---
layout: other
title: Install
permalink: /install/
---

<h2>{{"1. Download Repository"}}</h2>
<p>Can be found <a href="https://github.com/CPSECapstone/MicroPoly">here</a></p>

<h2>{{"2. Enter the Root Folder of the Project Directory"}}</h2>
* Using Powershell

<h2>{{"4. Start Data Collection, ML validation, and ML Server"}}</h2>
* Run: python mp-build.py
    * May need to update/install dotnet and python
    * Creates and starts the data collection task
    * Creates and starts the validation task and associated sub tasks
    * Setups up a server to request "good times" to update
        * Also adds a task to restart server if it goes down

<h2>5. Utilize HTTP Requests to Recieve "Good Times"</h2>
* Refer to <a href="/MicroPolyPages/demo/">the demo</a> for example requests and how to interpret responses

<h2>{{"[OPTIONAL] Uninstall MicroPoly"}}</h2>
* Run: python mp-uninstall.py
    * Will remove all created tasks
    * Can choose to remove all required python libraries
* On completion, can delete the root folder to fully uninstall

<br>
<p>If any issues are found, report them <a href="/MicroPolyPages/contact_issue_reporting/">here</a></p>
