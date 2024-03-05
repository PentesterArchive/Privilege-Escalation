# Capabilities enumeration
`getcap -r / 2>/dev/null` -> This command finds and lists enabled capabilities on the system.<br />
`getcap "/usr/bin/<binary>"` -> Shows the capabilities of the binary.<br />

After we have found the capabilities, we can refer to [GTFOBins](https://gtfobins.github.io/) to exploit them.<br />
