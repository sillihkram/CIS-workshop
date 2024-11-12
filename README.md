# RHEL-CIS-workshop
CIS-Ansible-Workshop

    sudo dnf install \
    rhel-system-roles
    openscap
    scap-security-guide
    ansible
    httpd

What is provided with the scap-security-guide package

    rpm -ql scap-security-guide 

Notice `scap-security-guide` provides open-scap security content to use with the binary as well as kickstart config files and ansible content. 

Let's see what security profiles are included with the RHEL9 Scap-Security-Guide (SSG) using the oscap binary to parse the XML file:

    oscap info /usr/share/xml/scap/ssg/content/ssg-rhel9-ds.xml


Let's target CIS Server lvl1 `xccdf_org.ssgproject.content_profile_cis_server_l1`

Now let's run a scan and save the results in xml and generate an HTML report.

    sudo oscap xccdf eval --profile xccdf_org.ssgproject.content_profile_cis_server_l1 --results-arf results.xml --report /var/www/html/index.html /usr/share/xml/scap/ssg/content/ssg-rhel9-ds.xml

Now that we've scanned our host let's review the results XML that we generated:

    sudo oscap info 

Look at the HTML report:
sudo systemctl start httpd
sudo firewall-cmd --add-service http 
sudo !! --perm


wc -l 
