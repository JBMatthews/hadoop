# Hadoop VM Setup Instructional Guide
<h3>VMWare</h3>
- XX</br>
<h3>CentOS Install</h3>
- With VMWare open, click “File” and then click “New”</br>
- Select “Create a custom virtual machine” and then click “Continue”</br>
- Select Linux > CentOS 64-bit and the click “Continue”</br>
- Make sure “Create a new virtual disk” and then click “Continue”</br>
- Before clicking “Finish” you must click the “Customize Settings” button</br>
- Name the file to be stored on your actual host machine something you’ll remember</br>
- Assemble “Sharing” options</br>
- Assemble “Processors & Memory” options</br>
    - Increase “Processors” to “4 processor core”</br>
    - Increase “Memory” to 10564MB </br>
- Select “Network Adapter” and select “Autodetect” under “Bridged Networking”</br>
- Click “Hard Disk (SCSI)” and increase Disk size to 1795.00GB and click “Apply”</br>
- Now, select “CD/DVD (IDE)” and click the “Connect…” box, and put your .iso file in the selection bar by selecting the drop-down menu option “Choose a disc…”</br>
- Select “Startup Disk” and then highlight “CD/DVD”  and now click “Restart…”</br>
<h3>CentOS Install Configuration</h3> 
- Make sure “Install CentOS 7” is highlight and the hit “Enter”</br>
- Select English, click “Continue”</br>
- Click “Installation Destination” > Conform HD is selected > Click “done”</br>
- Click “Network Adapter” > Under “Bridged Networking” select “Auto-detect”</br>
- Click “Network & Host Name” > Turn “Ethernet” on by switching slider “ON”</br>
- Click “Begin Installation”</br> 
- Click “ROOT PASSWORD” > Enter “hadoop” - Void “easy password warning” by clicking twice</br>
- Click “User Creation” and enter “training” and “hadoop”</br>
- Click “Finish Configuration” > Click “Reboot”</br>
- WAIT!</br>
<h3>KDE GUI Install</h3>
- Login as “root” using the password “hadoop”</br>
- Run [# yum -y groups install “KDE Plasma Workspaces”]</br>
    *This command will fail if ethernet/wifi connection is invalid. Return to “CentOS Install Configuration."</br>
- Once that finishes, run [# startx]</br>
    *Run successfully this command will bring you to your CentOS KDE GUI home screen.</br>
<h3>Install VMWare Tools</h3>
- From your CentOS KDE GUI home screen, open terminal “Konsole,” located under the “Kickoff Application Launcher”  pop up window.</br>
- Once terminal prompt is available, run [# yum install open-vm-tools]</br>
    *We have had mixed results install VMWare Tools. Mostly unsuccessful results though!</br>
<h3>Ambari Install from Repository</h3>
- Before attempting to install Ambari, make sure you have increased your instances memory capacity, as exampled in the “CentOS Installation” section above</br>
- Log in as “root” if you are not already</br>
- Download Ambari Repo file, by running [# wget -nv http://public-repo-1.hortonworks.com/ambari/centos6/2.x/updates/2.2.0.0/ambari.repo -O /etc/yum.repos.d/ambari.repo]</br>
    * Make sure you are downloading the most current Ambari repo being offered!</br>
- Confirm the repo in available for installs, by running [# yum repolist]</br>
- Install Ambari now, run [# yum ambari-server]</br> 
- Answer yes [y] to all questions</br>
- Setup Ambari server now by running [# ambari-server setup]</br>
- Respond to the setup prompts as follows:</br>
- SELinus Temp/ Disabled? [y]</br>
- Ambari runs as “root” by default? [n]</br>
- iptables Temp. Disabled? [y]</br>
- Select Java JDK version: Select from the list [1]</br>
- Accept License Agreement [enter]</br>
- Enter Advanced Database Configuration? [n]</br>
- Done! Check to see if ambari-server works by issuing the following commands:</br>
- [# ambari-server start]</br>
- [# ambari-server status]</br>
- [# ambari-server stop]</br>
<h3>Configuring Cluster</h3>
- Change your host file to include “puppet” by running:</br>
- [# cd /etc]</br>
- [# nano hosts]</br>
- Erase the line [localhost4 localhost4.localdomain] </br>
- Replace with [puppet], save and exit</br>
- Generate ssh keys and change appropriate permissions by following:</br>
- [# cd ~]</br>
- [# ssh-keygen]</br>
- [# cd .ssh]</br>
- [# cat id_rsa.pub >> “authorized_keys”]</br>
- [# chmod 640 authorized_keys]</br>
- [# cp id_rsa ../.]</br>
- [# cp authorized_keys ../.]</br>
<h3>Install MySQL</h3>
- xx</br>
<h3>Configuring Ambari in GUI</h3>
- In Firefox, type the following into your address bar [localhost:8080]</br>
- Enter the following username [admin] password [admin]</br>
- Click “??Install Config Wizard??” </br>
- Cluster name is: “training”</br>
- Select HDP version “HDP 2.3” from the stack selection</br>
- Under the “advance” setting dropdown un-select everything except “RedHat 7”</br>
- Click “Next”</br>
- Install Options:</br>
- Enter [localhost.localdomain] in “Target Hosts” section</br>
- Click “Browse” and select the .ssh key “id_rsa” from the menu </br>
    * If this command fails go back to “Configuring Cluster” above.</br>
- Click “Reg. & Con.”</br>
- Wait for loading completion, the click “Next”</br>
- Choose which Ambari services to install by selecting all EXCEPT the following:</br>
- Falcon</br>
- Kafka</br>
- Knox</br>
- Mahout</br>
- Slider</br>
-Smart Sense </br>
    * In our first-version we also de-selected: “Accumulo” and “Atlas”</br>
- Click, “Next”</br>
- Assign Master </br>
- Click, “Next”</br>
- Assign Slave </br>
- Click, “Next”</br>
- Customize Service section</br>
- Address issues (red alerts) </br>
- Enter “hadoop” as the password whenever requested.</br>
- Click, “Next” - A “warning” will pop-up, click “Proceed Anyway”</br>

