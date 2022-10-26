# ASRT Process Dissocation Procedures (PDP) Task created with jsPsych

<i>Created by the MEMO Team of Lyon Neuroscience Research Center (CRNL) (PI: Dezso Nemeth)</i>

<img src="static/logo_memo.png" height="100">

<h2>Citation</h2>
If you use the script, please include this citation in your manuscript:

Vékony, T. (2021). ASRT Process Dissociation Procedures Task created with jsPsych (Version 1.0.0) [Computer software]. https://doi.org/10.5281/zenodo.7253644
<a href="https://doi.org/10.5281/zenodo.7253644"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.7253644.svg" alt="DOI"></a>

<h2>About the task</h2>

A Process Dissociation Procedures Task for the <a href="https://github.com/vekteo/ASRT_JSPsych">ASRT paradigm</a> created with the jsPSych library (<a href="https://link.springer.com/article/10.3758/s13428-014-0458-y">de Leeuw, J. R., 2015</a>).

The task consists of two main parts. In the first part, users are asked to try to type the sequence they see in the ASRT task. In the second part, they are asked to enter a sequence that they did not see in the ASRT task. Now the appearance of the stimuli is controlled by the users. The response buttons are the same as in the main task and the stimuli are displayed according to the keypresses.

Each section consists of 4 blocks. Each block is completed after 24 valid keypresses (the 25th keypress exits the block).

<h2>Output variables</h2>
<li><strong>browser_events:</strong> browser events at the given trial (fullscreenenter, fullscreenexit, blur or focus)</li>
<li><strong>view_history:</strong> only relavant at the 'instructions'; the actions and the corresponding RTs when the instruction trials are presented</li>
<li><strong>subject:</strong> A 15-character long random subject ID for the online version, and customized subject number for the offline version</li>
<li><strong>session:</strong> customized session number (for offline version only)</li>
<li><strong>rt:</strong> reaction time (RT) in ms - it indicates the RT from the previous button press</li>
<li><strong>trial_type:</strong> the JSPSych trial type of the given trial ('instructions', 'html-keyboard-response' or 'serial-reaction-time')</li>
<li><strong>trial_index:</strong> the number of the given trials (all events considered, even instructions too!)</li>
<li><strong>time_elapsed:</strong> the time elapsed from the start of the program in ms</li>
<li><strong>internal_code_id:</strong> internal node id of the trial</li>
<li><strong>stimulus:</strong> stimulus on the screen; relevant only if instructions are present</li>
<li><strong>key_press:</strong> the JS code of the key pressed</li>
<li><strong>grid:</strong> layout of the circle positions (in a grid)</li>
<li><strong>target:</strong> position of stimulus on the screen (as a result of the previously pressed button) (the four positions: 0: 0,0; 1: 0,1; 2: 0,2; 3: 0,3)</li>
<li><strong>test_part:</strong> indicates if the trial is part of a valid reponse or if it is the last quitting button press ('valid_button_press', 'last_quitting_trial')</li>
<li><strong>block:</strong> number of the block (1-4)</li>
<li><strong>trial_number:</strong> the number of the element in the response (0-24, only valid responses from 0-23)</li>
<li><strong>response_key:</strong> the pressed response key ('s', 'f', 'j',  'l')</li>
<li><strong>response_button:</strong> the number of the pressed response button (0-3)</li>
<li><strong>task_type:</strong> the type of the task ('inclusion', 'exclusion')</li>

<h2>Setting options</h2>
<p>The language of the task can be set in the <i>parameters.js</i> file. Available languages: english (en), hungarian (hu), french (fr), portuguese (pt)</p>

<h2>How to start the task</h2>
Open the <i>index.html</i> file in either the <i>offline</i> or <i>online</i> folder. When the offline version is started, you can customize the subject and session numbers (any number is accepted). If you start the offline version, a random subject ID will be allocated.

<h2>Browser requirements</h2>
<p>Any browser except Safari and Internet Explorer. Recommended: Chrome</p>

<h2>Analysis</h2>
To analyze the data, use the PDP_analysis notebook. With the help of the notebook, you can calculate the proprotion of high probability triplets separetely in the inclusion vs. exclusion conditions.
