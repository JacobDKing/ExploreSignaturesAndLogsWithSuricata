# Signature And Log Analysis With Suricata
The purpose of this project is to demonstrate knowledge of the components of rules within Suricata. We also demonstrate triggering a new rule and examining the output in Suricata by using a Bash shell. <br />

Tasks:
  - Examine a rule in Suricata.
  - Trigger a rule and review the alert logs.
  - Examine 'eve.json' outputs.

<h2>Examining a Custom Rule in Suricata</h2>
In this step, we explore the current composition of the Suricata rule defined in the "custom.rules" file.

<img src="https://i.imgur.com/YObXJ9Y.png" height="80%" alt="Examining a custom rule1"/> <br />

  - The action is the first part of the signature. It determines the action to take if all conditions are met.
  - The next part of the signature is the header. The header defines the signature’s network traffic, which includes attributes such as protocols, source and destination IP addresses, source and destination ports, and traffic direction.
  - The following section, rule options, allow you to customize signatures with additional parameters.

<br />
<br />

<h2>Triggering a Custom Rule in Suricata</h2>
In this section, we'll trigger a custom Suricata rule and examine the alert logs that Suricata generates. <br />

  - Run Suricata and list files in /var/log/suricata folder:
<img src="https://i.imgur.com/m18J9nK.png" height="80%" alt="List Files1"/> <br />
<img src="https://i.imgur.com/reJ55Gh.png" height="80%" alt="List Files2"/> <br /> <br />
Note that there are a total of 4 files with the same "read, write, & execute" permissions for file owners, group owners, and other users.

  - Use the 'cat' command to display the fast.log file generated by Suricata:
<img src="https://i.imgur.com/cRW45Es.png" height="80%" alt="Display fast.log"/> <br />

<br />
<br />

<h2>Examine eve.json Output</h2>
In this section, we examine the additional output that Suricata generates in the eve.json file. <br />

  - Use 'cat' command to display entries in the eve.json file:
<img src="https://i.imgur.com/RiBUOGH.png" height="80%" alt="Display eve.json entries"/> <br />
Note that there is a lot of data returned that is not easy to understand in this format.

  - Use 'jq' command to display entries in an improved format:
<img src="https://i.imgur.com/lIcNhl9.png" height="80%" alt="Display eve.json entries 2"/> <br />
Note that you must exit the 'less' command using "Q" to return to command-line prompt.

  - Use 'jq' command to extract specific event data from eve.json file:
<img src="https://i.imgur.com/HJfi1Af.png" height="80%" alt="Display eve.json entries 3"/> <br />

  - Use 'jq' command to display all event logs related to a specific flow_id from the eve.json file:
<img src="https://i.imgur.com/FzraWSa.png" height="80%" alt="Display eve.json entries 4"/> <br />


<br />
<br />

<h4>End of Project</h4>
