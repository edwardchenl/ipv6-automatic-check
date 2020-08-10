# ipv6-automatic-check
include TCP and HTTP application check

tcp check usage:
You can add a cron to do automatic check and export the check report to the dictionary n
*/15 * * * * python3 /root/ipv6_tcp_check.py 2400::1 80 'test123' 'ok' dictionary

http check usage:
The HTTP check add host option than tcp.
*/15 * * * * python3 /root/ipv6_http_check.py 2400::1 80 'GET / HTTP/1.1' 'Host:[2400::1]' '200' dictionary
