# audit
The Linux kernel logs a lot of things but by default it doesn't log TTY input. The audit log allows sysadmins to log this. If logging of TTY input is enabled, any
input including passwords are stored hex-encoded inside /var/log/audit/audit.log . We can decode these values manually or use the aureport utility to query and retrieve
records of TTY input. To learn more about PAM TTY see this page. 
</br>Let's query all TTY logs.</br>
![2](https://github.com/alejandro-pentest/Hacking-Web/assets/161533623/358d69b8-c2b2-4d55-83a2-b1d0b189cf6d)

<img src="https://github.com/alejandro-pentest/Hacking-Web/assets/161533623/358d69b8-c2b2-4d55-83a2-b1d0b189cf6d" width="600">


The TTY report reveals that the mrb3n user logged in with the password mrb3n_Ac@d3my! using su. Let's do the same. </br>
[aureport - Install and use](https://ubunlog.com/aureport-resumenes-registros-sistema/).</bd>
[Creating Audit Reports - Red Hat](https://access.redhat.com/documentation/es-es/red_hat_enterprise_linux/7/html/security_guide/sec-creating_audit_reports).</br>
![3](https://github.com/alejandro-pentest/Hacking-Web/assets/161533623/c27f8560-36c8-4175-94be-eeb4d5bbe60d)
