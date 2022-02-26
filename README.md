<h2 align="center">☢️ Log4j-scanner ☢️</h2>

<h4 align="center">Scan the log4j vulnerability with the log4j scanner tool.</h4>

<h2 align="center">Features 👻</h2>

   - Features and advantages that exist in this tool:
     - Support for lists of URLs.
     - Fuzzing for more than 60 HTTP request headers (not only 3-4 headers as previously seen tools).
     - Fuzzing for HTTP POST Data parameters.
     - Fuzzing for JSON data parameters.
     - Supports DNS callback for vulnerability discovery and validation.
     - WAF Bypass payloads.

<h2 align="center">Usage</h2>

```python
$ python3 log4j-scan.py -h
[•] CVE-2021-44228 - Apache Log4j RCE Scanner
[•] Scanner provided by FullHunt.io - The Next-Gen Attack Surface Management Platform.
[•] Secure your External Attack Surface with FullHunt.io.
usage: log4j-scan.py [-h] [-u URL] [-p PROXY] [-l USEDLIST] [--request-type REQUEST_TYPE] [--headers-file HEADERS_FILE] [--run-all-tests] [--exclude-user-agent-fuzzing]
                     [--wait-time WAIT_TIME] [--waf-bypass] [--custom-waf-bypass-payload CUSTOM_WAF_BYPASS_PAYLOAD] [--test-CVE-2021-45046]
                     [--dns-callback-provider DNS_CALLBACK_PROVIDER] [--custom-dns-callback-host CUSTOM_DNS_CALLBACK_HOST] [--disable-http-redirects]

optional arguments:
  -h, --help            show this help message and exit
  -u URL, --url URL     Check a single URL.
  -p PROXY, --proxy PROXY
                        send requests through proxy
  -l USEDLIST, --list USEDLIST
                        Check a list of URLs.
  --request-type REQUEST_TYPE
                        Request Type: (get, post) - [Default: get].
  --headers-file HEADERS_FILE
                        Headers fuzzing list - [default: headers.txt].
  --run-all-tests       Run all available tests on each URL.
  --exclude-user-agent-fuzzing
                        Exclude User-Agent header from fuzzing - useful to bypass weak checks on User-Agents.
  --wait-time WAIT_TIME
                        Wait time after all URLs are processed (in seconds) - [Default: 5].
  --waf-bypass          Extend scans with WAF bypass payloads.
  --custom-waf-bypass-payload CUSTOM_WAF_BYPASS_PAYLOAD
                        Test with custom WAF bypass payload.
  --test-CVE-2021-45046
                        Test using payloads for CVE-2021-45046 (detection payloads).
  --dns-callback-provider DNS_CALLBACK_PROVIDER
                        DNS Callback provider (Options: dnslog.cn, interact.sh) - [Default: interact.sh].
  --custom-dns-callback-host CUSTOM_DNS_CALLBACK_HOST
                        Custom DNS Callback Host.
  --disable-http-redirects
                        Disable HTTP redirects. Note: HTTP redirects are useful as it allows the payloads to have a higher chance of reaching vulnerable systems.
```

<h2 align="center">Way of work</h2>

```
$ python3 log4j-scan.py -u https://domain.com
```
