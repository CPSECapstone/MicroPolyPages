---

layout: home
---
<h2>The Problem:</h2>
* Many Windows background updates can disrupt user activities
* Taking computer resources at inopportune times can be frustrating
* For example:
   * Some Operating System updates might affect a user’s game experience, as the update takes some CPU away from the game.
   * A sound driver update in the middle of a user’s Zoom call could drastically affect their meeting.

<h2>The Current Solution:</h2>
* Windows Active Hours
   * Can tell your computer when you are actively using it (Static period for everyday)
   * Informs update orchestrator and schedules update, install, reboot.
* Limitations:
   * A user may have an inconsistent schedule
   * Students/Teachers use devices more during school year
   * Use device more/less on weekends
   * Health conditions interfere (Sleeping problems)
   * There is a need for scheduler to determine a “good time” to update for each user

<h2>Proposed Solution:</h2>
<h3>Features:</h3>
* Improves update timing by adapting to device use over time using a machine learning model, XGBoost.
* Supports retraining of the ML model
* Utilizes a scheduled task to collect user data (Runs every 5 minutes)
    * System Logs
    * Device State
    * CPU utility
    * etc
* Provides an API for the Windows Update Orchestrator to hit the endpoints and determine when to schedule an update, and whether or not right now is a good time to update.
* Tracks the accuracy of the model's performance over time.

<h3>MicroPoly API</h3>
* A RESTful API hosted on the local machine that can be queried to provide a list of good times to install an update, OR to check if the device has the capacity to install the current update now. 
* The API references several XGBoost models that uses time series forecasting to predict the device’s resource usage for the next day, and uses heuristics from the thresholds provided in the request to determine “good times”.

<h3>Technical Requirements:</h3>
* The system shall run on machines with a supported version of Windows (10 and 11 as of date) as an executable
* The ML model shall not exceed 150 MB in size
* The ML model shall evaluate in 2 seconds or less
* The system shall support Win32 calls or other standard query calls

<h2>Docs</h2>
* You can find our final presentations from every quarter, final project architectures, and the MicroPoly Technical Specification in the README of the [GitHub Repo](https://github.com/CPSECapstone/MicroPoly). There is also information on recompiling the production executable.
