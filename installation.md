---
layout: other
title: Install
permalink: /install/
---

<h2>{{"1. Download Repository"}}</h2>
<p>Can be found <a href="https://github.com/CPSECapstone/MicroPoly">here</a></p>

<h2>{{"2. Enter the root folder of the project directory"}}</h2>

<h2>{{"3. Install required dependencies"}}</h2>
* Use: pip install -r requirements.txt

<h2>{{"4. Start data collection and ML server"}}</h2>
* Use: python mp-build.py
    * creates and starts the data collection task
    * setups up a server to request "good times" to update

<h2>5. Utilize HTTP requests to recieve "good times"</h2>
* Refer to <a href="/MicroPolyPages/demo/">the demo</a> for example requests and how to interpret responses

<h2>6. Changing the file path from test data to rolling data</h2>
* Change line 9 in 'apiServer.py' from "app = create_app(config.ApiDevelopmentConfig)" to "app = create_app(config.ApiProductionConfig)"
<br>
<p>If any issues are found, report them <a href="/MicroPolyPages/contact_issue_reporting/">here</a></p>
