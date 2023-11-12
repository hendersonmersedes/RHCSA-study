# RHCSA-study
Study notes for the exam.
<h2>Resources: I am using the Sander van Vugt course and his RHCSA 9 textbook to prepare for this exam.</h2>

<h3>Configure Users and Permissions</h3>
<h3>Creating Partitions</h3>
<p><img src="Screenshot 2023-08-27 213830.png"></p>
<h3> Make File System</h3>
<p><img src= "mkfs.png"></p>
<h3> Unmount a mounted filesystem </h3>
<p><img src ="unmount.png"></p> 
<h3> Create a Swap</h3>
<p><img src ="swap.png"></p>
<h3> Resize Logical Volumes and Volume Groups</h3>
<p><img src="lvmgroups.png"</p>
<h3>Schedule Jobs</h3>
<p>Schedule jobs to run  on a repeating schedule with a user's crontab file. </p>
<p> "man at" shows how to execute schedule jobs. These are one time jobs. For example: "at now +3min" runs a job 3 min from now.</p>
<p>"atq" lists scheduled jobs. "atrm" removes the job.</p>
<p>Recurring Jobs: The crond daemon reads multiple config files. Each user has a personal file that they edit with "crontab -e". The fields in the crontab file are in the following order:
<p><ul>
  <li>Minutes</li>
  <li>Hours</li>
  <li>Day of Month</li>
  <li>Month</li>
  <li>Day of Week</li>
  <li>Command</li>
</ul></p></p>
<h3>Manage Temporary Files</h3>
<p>Red Hat includes the systemd-tmpfiles tool - provides a method to manage temporary directories and files. The systemd-tmpfiles-setup service runs the systemd-tmpfiles command.</p>
<p>systemd-tmpfiles-clean service configuration files exist in three places:
/etc/tmpfiles.d/*.conf
/run/tmpfiles.d/*.conf
/usr/lib/tmpfiles.d/*.conf</p>
<h3>Analyze and Store Logs</h3>
<p>The rsyslog service is used to determine for handle log messages. </p>
<p>The logrotate command rotates log files to prevent them from taking too much space in the /var/log directory. When a log is rotated, it is renamed with an extension.</p>
