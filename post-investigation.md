Post-Compromise Investigation

After detecting the successful RDP login (Event ID 4624), further investigation was conducted to identify potential persistence or lateral movement.

The following Windows Security Events were reviewed:

  - 4720 – User account creation

  - 4732 – User added to privileged group

  - 5145 – Access to shared objects

  - 4688 – Process creation

  - 5140 - Access to internal folders

No suspicious post-compromise activity was identified.
