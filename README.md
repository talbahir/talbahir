# talbahir
Purpose: automatically add offenders IPs to ufw deny rule

  It scans error.log and access.log for "not found or unable to stat" and 404 respectably.
  
  When find IPs with occurance > nMax will add rull to ufw deny rule
  
  Save in /usr/local/bin/banip, chmod +x it, and schedule add to crontab the follow:
  
  ban IPs with excesss number of 404
  
  */10 * * * * /usr/local/bin/banip
  
  You check log:
  
  cat /var/log/banIP.log to see last run or 
  
  cat /var/log/banips.log to see banned IPs
  
