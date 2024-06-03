---
layout: other
title: Install
permalink: /install/
---

<h2>{{"1. Download Repository"}}</h2>
<p>Can be found <a href="https://github.com/CPSECapstone/MicroPoly">here</a></p>

<h2>{{"2. Enter the root folder of the project directory"}}</h2>
* Using Powershell (cd MicroPoly)

<h2>{{"3. Install required dependencies"}}</h2>
* Run: python --version (Should be Python 3.11+; Else upgrade)
* Run: winget install Microsoft.DotNet.SDK.8
* Run: curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py \| python get-pip.py

<h2>3.5. Set MicroPoly to run in production mode</h2>
* Run: $env:PRODUCTION_TESTING="true"
    * sets use of production/rolling data file

<h2>{{"4. Start data collection and ML server"}}</h2>
* Run: python mp-build.py
    * installs all the python requirements
    * creates and starts the data collection task
    * setups up a server to request "good times" to update
    * creates and starts the validation caching task(s).

<h2>5. Utilize HTTP requests to recieve "good times"</h2>
* Refer to <a href="/MicroPolyPages/demo/">the demo</a> for example requests and how to interpret responses

<br>
<p>If any issues are found, report them <a href="/MicroPolyPages/contact_issue_reporting/">here</a></p>
