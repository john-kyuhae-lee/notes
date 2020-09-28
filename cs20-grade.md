
### MSEL 24.00.01 Receive Daily INTSUM
<table>
  <tr>
    <td>**Measure**</td>
    <td>ID.AM-1.1</td>
  </tr>
  <tr>
    <td>**Description**</td>
    <td>Perform Vulnerability scan of network</td>
  </tr>
  <tr>
    <td colspan=2> **Expected Action** </td>
  </tr>
  <tr>
    <td colspan=2> ```1) Team member verifies network connectivity to a network.
2) Team member assures the vulnerability assessment tool is using the latest updates and signatures of the selected tool.
3) Team member scans a network and identifies all hosts / systems on network enclave.
4) Team member configures the vulnerability assessment tool with the IP address of the network enclave.
5) Team member selects assessment options within the tool based on testing level required. (Note: Some tests can cause denial of service to host and will need to be evaluated before beginning of assessment.)
6) Team member runs the assessment with selected options and monitors progress.
7) Team member evaluates the results of the assessment and determines if critical or high vulnerabilities exist on the test machine.
``` </td>
  </tr>
  <tr>
    <td>**Grade**</td>
    <td>Meets Standard</td>
  </tr>
  <tr>
    <td>**Comment**</td>
    <td>Meets Standard</td>
  </tr>
</table>

| **Measure** | ID.AM-1.2 |
|-|-|
| **Description** | Determine DNS names for all network hosts |
<td colspan=2> **Expected Action**
<td colspan=2> ```#gather list of computers
Get-ADComputer -filter * -properties Name | Export-Csv new_pc_dump.csv
#add white space and title
echo " " >> .\Domain_Changes_Log.txt
echo " " >> .\Domain_Changes_Log.txt
echo "PCs Checked" >> .\Domain_Changes_Log.txt
#add date time stamp
get-date >> .\Domain_Changes_Log.txt
#compare known good to new list then add new computers to the log file
Compare-Object $(Get-Content .\Known_good_pc_list.csv) $(Get-Content .\new_pc_dump.csv) >> .\Domain_Changes_Log.txt
#Generate pop-up box if there is a change.
if ((Compare-Object $(Get-Content .\Known_good_pc_list.csv) $(Get-Content .\new_pc_dump.csv)) -ne $null)
{ [System.Reflection.Assembly]::LoadWithPartialName("System.Windows.Forms")
 $oReturn=[system.windows.forms.messagebox]::show("Domain Computer added! This change needs to be verified and the master list updated.")
}
| **Grade** | Meets Standard |
|**Comment**| Team enumerated DNS names according to the DCOE Battle Drill.

22SEP2020 JKL |

| **Measure** | ID.AM-2.1 |
|-|-|
| **Description** | Review Organizational User Policies |
<td colspan=2> **Expected Action**
<td colspan=2> ```1) The team member reviews all written policies regarding users of information systems within a given organization. The policies should at a minimum address:

A. Acceptable Use Policy
B. Account request process
C. Account creation/deletion/suspension procedures
D. Access control methodology (e.g. group membership)
E. Initial and periodic user training
F. Process for elevated privilege request and review
G. Account audit process

2) Team member will interview information security personnel to ensure complete understanding of policies and technical implementation as necessary.
3) The team member interviews random knowledge workers to ensure user base has full understanding of user requirements and responsibilities.
```
| **Grade** | Needs Improvement |
|**Comment**| Team did not produce Organizational User Policy review with risk mitigation plan. |

johnk@DESKTOP-L7T3DS7 C:\Users\johnk\cybershield20
$ python .\parse_raw_dump.py
### MSEL 24.00.01 Receive Daily INTSUM
| **Measure** | ID.AM-1.1 |
|-|-|
| **Description** | Perform Vulnerability scan of network |
|<td colspan=2> **Expected Action**
|<td colspan=2> ```1) Team member verifies network connectivity to a network.
2) Team member assures the vulnerability assessment tool is using the latest updates and signatures of the selected tool.
3) Team member scans a network and identifies all hosts / systems on network enclave.
4) Team member configures the vulnerability assessment tool with the IP address of the network enclave.
5) Team member selects assessment options within the tool based on testing level required. (Note: Some tests can cause denial of service to host and will need to be evaluated before beginning of assessment.)
6) Team member runs the assessment with selected options and monitors progress.
7) Team member evaluates the results of the assessment and determines if critical or high vulnerabilities exist on the test machine.
```
| **Grade** | Meets Standard |
|**Comment**| Meets Standard |

| **Measure** | ID.AM-1.2 |
|-|-|
| **Description** | Determine DNS names for all network hosts |
|<td colspan=2> **Expected Action**
|<td colspan=2> ```#gather list of computers
Get-ADComputer -filter * -properties Name | Export-Csv new_pc_dump.csv
#add white space and title
echo " " >> .\Domain_Changes_Log.txt
echo " " >> .\Domain_Changes_Log.txt
echo "PCs Checked" >> .\Domain_Changes_Log.txt
#add date time stamp
get-date >> .\Domain_Changes_Log.txt
#compare known good to new list then add new computers to the log file
Compare-Object $(Get-Content .\Known_good_pc_list.csv) $(Get-Content .\new_pc_dump.csv) >> .\Domain_Changes_Log.txt
#Generate pop-up box if there is a change.
if ((Compare-Object $(Get-Content .\Known_good_pc_list.csv) $(Get-Content .\new_pc_dump.csv)) -ne $null)
{ [System.Reflection.Assembly]::LoadWithPartialName("System.Windows.Forms")
 $oReturn=[system.windows.forms.messagebox]::show("Domain Computer added! This change needs to be verified and the master list updated.")
}
```
| **Grade** | Meets Standard |
|**Comment**| Team enumerated DNS names according to the DCOE Battle Drill.

22SEP2020 JKL |

| **Measure** | ID.AM-2.1 |
|-|-|
| **Description** | Review Organizational User Policies |
|<td colspan=2> **Expected Action**
|<td colspan=2> ```1) The team member reviews all written policies regarding users of information systems within a given organization. The policies should at a minimum address:

A. Acceptable Use Policy
B. Account request process
C. Account creation/deletion/suspension procedures
D. Access control methodology (e.g. group membership)
E. Initial and periodic user training
F. Process for elevated privilege request and review
G. Account audit process

2) Team member will interview information security personnel to ensure complete understanding of policies and technical implementation as necessary.
3) The team member interviews random knowledge workers to ensure user base has full understanding of user requirements and responsibilities.
```
| **Grade** | Needs Improvement |
|**Comment**| Team did not produce Organizational User Policy review with risk mitigation plan. |
