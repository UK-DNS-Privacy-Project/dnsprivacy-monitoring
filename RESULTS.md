## dnsprivacy.org monitoring results
 
Latest run at:  Sat Apr 19 02:54:43 UTC 2025
 
See [the output of the latest workflow for more details](https://github.com/dnsprivacy/dnsprivacy-monitoring/actions/workflows/dnsprivacy-monitoring.yml)

|Server and IP version|TLS|TLS 443| Strict Name| Strict Name 443| Cert 0| Cert 14| QNAME min| RTT 250| DNSSEC| Keepalive| Padding| TLS 1.3| OOOR |
| ---  | --- |---  | ---         |---            | ---   |---     | ---      |---     | ---    |---      | ---    |---     | ---  |
| resolver-1.dnsprivacy.org.uk  (v4) |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :x:  |  :x:  |  :white_check_mark:  |  :x:  |
| resolver-1.dnsprivacy.org.uk  (v6) |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :x:  |  :x:  |  :white_check_mark:  |  :x:  |
| resolver-2.dnsprivacy.org.uk  (v4) |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :x:  |  :x:  |  :white_check_mark:  |  :x:  |
| resolver-2.dnsprivacy.org.uk  (v6) |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :x:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :white_check_mark:  |  :x:  |  :x:  |  :white_check_mark:  |  :x:  |
####  All the following are tested over TLS connections:

 * **TLS** Does the server answer DNS queries over TLS on port 853 with no SNI sent?
 * **TLS 443** Does the server answer DNS queries over TLS on port 443 with no SNI sent?
 * **Strict Name** Does the server pass Strict authentication using the authentication domain name only?
 * **Strict Name 443** Does the server pass Strict authentication using the authentication domain name only on 443 (some operators require an SNI on 443 to defend against attacks)?
 * **Cert 0** Are there 0 days or less to certificate expiry?
 * **Cert 14** Are there 14 or fewer days to certificate expiry?
 * **QNAME min** Is the server configured to use QNAME minimisation [RFC7816]?
 * **RTT 250** Is a simple query round trip time from the probe location < 250ms?
 * **DNSSEC** Is the server doing DNSSEC validation (i.e. returning SERVFAIL for bogus domains)?
 * **Keepalive** Does the server support the EDNS0 Keepalive option [RFC7828]?
 * **Padding** Does the server add an EDNS0 Padding option to the response if one is in the query [RFC7830]?
 * **TLS 1.3** Does the server support TLS 1.3 ?
 * **OOOR** Does the server give Out Of Order Responses (Experimental, may give false negatives)?

Authentication information is taken from the [DNS Privacy Project Test Servers](https://dnsprivacy.org/wiki/display/DP/DNS+Privacy+Test+Servers) page. These tests use getdns_server_mon, a [getdns based monitoring plugin](https://github.com/getdnsapi/getdns/tree/develop/src/tools).

Note that Quad9, Cloudflare and Google and others operate an anycast service so the results below are just for the location of the Github test runner used for the test.

