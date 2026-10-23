# Burp-Suite-Temp-Recovery
Burp Suite Temp/*.tmp files Recovery Recover requests, responses and strings from leftover Burp Suite temp files. Everything is parsed in your browser; nothing is uploaded. Standalone HTML webapp.

# What the app does

* You can drop in raw temp files or a .zip (`/tmp/burp*` linux / `%TEMP%/burp*` - Windows) . It scans for records with that length framing.
* If a record was cut off by the crash, it carves HTTP requests and responses out of the raw bytes instead.
* It pairs each request with its response and lists them with host, method, URL and status.
* It also lists loose strings, and it flags anything that mentions oastify.com or burpcollaborator.net as a possible Collaborator record.
* Selecting a record shows the request, the response and a hex view. Gzip response bodies are decompressed automatically.
* You can copy or save a single record, or export everything shown as JSON. The filter box searches host and URL.

All parsing happens in your browser and nothing is uploaded, which matters for client traffic.

# Live
https://saphir.berlin/BurpTempRecovery.html
