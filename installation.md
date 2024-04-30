---
layout: other
title: Install
permalink: /install/
---

<h2>{{"1. Download Repository"}}</h2>
<p>Can be found <a href="https://github.com/CPSECapstone/MicroPoly">here</a></p>

<h2>{{"2. Enter the root folder of the project directory"}}</h2>
* Using Powershell

<h2>{{"3. Install required dependencies"}}</h2>
* Run: pip install -r requirements.txt

<h2>3.5. Changing the file path from test data to rolling data</h2>
* Run: $env:PRODUCTION_TESTING="true"
    * sets use of production/rolling data file

<h2>{{"4. Start data collection and ML server"}}</h2>
* Run: python mp-build.py
    * creates and starts the data collection task
    * setups up a server to request "good times" to update

<h2>5. Utilize HTTP requests to recieve "good times"</h2>
* Refer to <a href="/MicroPolyPages/demo/">the demo</a> for example requests and how to interpret responses

<br>
<p>If any issues are found, report them <a href="/MicroPolyPages/contact_issue_reporting/">here</a></p>
