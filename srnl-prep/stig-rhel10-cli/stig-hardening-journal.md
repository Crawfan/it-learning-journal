# STIG Hardening Journal — RHEL 10 CLI (Week of 2025-07-17)

## 🧠 Goal

To evaluate the security posture of a cloned RHEL 10 virtual machine using the official DISA
STIG baseline, executed via the `oscap` CLI tool. This was part of my SRNL preparation to
practice system hardening and risk assessment per NIST 800-53 compliance objectives.

---

## 🔧 Tools & Resources

- **Operating System:** Red Hat Enterprise Linux 10 (cloned VM)
- **Tools Installed:** `openscap`, `scap-security-guide`
- **Profile Used:** `xccdf_org.ssgproject.content_profile_stig`
- **Data Source:** `/usr/share/xml/scap/ssg/content/ssg-rhel10-ds.xml`
- **Output Files:** 
  - `stig-results.xml` (machine-readable)
  - `stig-report.html` (human-readable summary)
- **Reference Docs:** 
  - DISA STIG downloads: https://public.cyber.mil/stigs/
  - NIST 800-53: Security and Privacy Controls for Federal Information Systems

---

## 🛠️Steps Taken

### 1.  Cloned Original RHEL 10 VM
To avoid modifying my clean install, I cloned the base RHEL VM using VirtualBox’s disk
duplication feature.

```bash
VBoxManage clonevm "rhel10-base" --name "rhel10-stig-test" --register
```

### 2. Installed OpenSCAP and the STIG content provided by scap-security-guide
	sudo dnf install openscap openscap-utils scap-security-guide -y

### 3. Ran STIG CLI Evaluation
- executed the stig scan using the command below. This uses a predefined DISA profile
mapped to RHEL 10 standards 
	sudo oscap xccdf eval \
		 --profile xccdf_org.ssgproject.content_profile_stig \
		 --results ./stig-results.xml \
		 --report ./stig-report.html \
	 /usr/share/xml/scap/ssg/content/ssg-rhel10-ds.xml

### 4. Reviewed Scan Output
- Total Rules Evaluated: 474
- Passed:189
- Failed:285
- Skpped:0
	Results were saved in stig-results.xml (machine readable) and stig-report.html 
	(Visual summary with pass/fail breakdowns)
