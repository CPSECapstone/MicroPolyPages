---
layout: other
title: Install
permalink: /install/
---

<h2>{{"1. Download Repository"}}</h2>
<p>Can be found <a href="https://github.com/CPSECapstone/MicroPoly">here</a></p>

<h2>{{"2. Enter the Root Folder of the Project Directory"}}</h2>
* Using Powershell or an IDE of your choice.

<h2>{{"3. Start Data Collection, API server, and ML validation"}}</h2>
<h3>Alpha Release (Development Mode)</h3>
* Run: python mp-build.py
    * May need to update/install dotnet and python (refer to part 3.5 then return to part 3)
    * Creates and starts the data collection task
    * Sets up a local HTTP server to request "good times" to update
    * Creates and starts the validation task and associated sub tasks
    * Gives very meaningful error messages/logs in case the application does not run as expected.

<h3>Beta Release (Production Mode)</h3>
* Run: start ./production-install.exe
    * Creates and starts the data collection task
    * Sets up a local HTTP server to request "good times" to update
        * Sets up a task to restart the server on login (Server does not persist after a shutdown)
    * Creates and starts the validation task and associated sub tasks
    * Will ask for administrator priviledges. 

<h2>{{"3.5. Install Required Dependencies (If Needed)"}}</h2>
* Run: python --version (Should be Python 3.12+; Else upgrade)
* Run: winget install Microsoft.DotNet.SDK.8
* Run: curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py \| python get-pip.py

<h2>4. Utilize HTTP Requests to Recieve "Good Times"</h2>
* Refer to <a href="/MicroPolyPages/demo/">the demo</a> for example requests and how to interpret responses

<h2>{{"[OPTIONAL] Uninstall MicroPoly"}}</h2>
* Run: python mp-uninstall.py
    * Will remove all created tasks, whether you chose to run the dev or production release.
    * Can choose to remove all required python libraries installed at build time
    * Can choose to remove all data created at runtime (In out folder)
* On completion, can delete the root folder to fully uninstall

<br>
<p>If any issues are found, report them <a href="/MicroPolyPages/contact_issue_reporting/">here</a></p>
