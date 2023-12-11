# C кешем
Running 10s test @ http://localhost:8081/
  2 threads and 2 connections\
|Thread Stats   |Avg        |Stdev     |Max     |+/- Stdev
|---------------|-----------|----------|--------|----------
| Latency       |1.43ms     |1.50ms    |15.40ms | 82.00%
|Req/Sec        |0.86k      |723.79    |1.96k   |67.50%

|Latency  |Distribution
|---------|-----------
|     50% | 599.00us
|     75% | 2.24ms
|     90% | 3.57ms
|     99% | 6.13ms

  17057 requests in 10.01s, 849.52KB read
  Socket errors: connect 0, read 17057, write 0, timeout 0
  Non-2xx or 3xx responses: 17057
Requests/sec:   1704.03
Transfer/sec:     84.87KB
# Без кеша
Running 10s test @ http://localhost:8081/
  2 threads and 2 connections

|  Thread Stats|   Avg    |  Stdev  |   Max   |+/- Stdev
|--------------|----------|---------|---------|---------
|    Latency   |1.55ms    |1.71ms   |20.21ms  | 82.60%
|    Req/Sec   |836.53    |726.94   |1.93k    |  65.00%

|Latency |Distribution
|--------|-------------
|50%     |597.00us
|75%     |2.44ms
|90%     |4.08ms
|99%     |6.94ms

  16656 requests in 10.01s, 829.60KB read
  Socket errors: connect 0, read 16656, write 0, timeout 0
  Non-2xx or 3xx responses: 16656
Requests/sec:   1664.54
Transfer/sec:     82.91KB