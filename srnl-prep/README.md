# RHEL 10 STIG CLI SCAN (oscap)

**Date:** 2025-07-17
**Objective:** Run DISA STIG profile on a RHEL 10 clone using CLI (oscap)
**Tools Used:** `openscap`, `scap-security-guide`

## Steps Taken
1. Installed SCAP tools via:
     `sudo dnf install openscap openscap-utils scap-security-guide -y`
2. Ran STIG profile with:
     ```bash 
     sudo oscap xccdf eval \
	--profile xccdf_org.ssgproject.content_profile_stig \
	--results ./stig-results.xml \
	--report ./stig-report.html \
	/usr/share/xml/scap/ssg/content/ssg-rhel10-ds.xml
     ```
3. reviewed report --> found 
     Pass: 189
     Fail: 285
     Skipped: 0
   (see attached `stig-report.html`)
