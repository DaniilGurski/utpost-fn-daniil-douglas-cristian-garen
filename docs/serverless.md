## steg 0

### före

äter http://localhost:4000: 10 samtidiga uppladdningar à 4000x3000, health var 100:e ms …

| Vad                            | p50   | max    |                        |
| ------------------------------ | ----- | ------ | ---------------------- |
| Uppladdning (POST /api/photos) | 50 ms | 101 ms | 0/10 ok                |
| Health (GET /api/health)       | –     | –      | 0 anrop                |
| processingMs (bildarbetet)     | –     | –      | saknas i svaret        |
| apiMs (API:ets totala tid)     | –     | –      | saknas i svaret (före) |

Total tid: 108 ms · kallstarter i svaren: 0

### efter

| Vad                            | p50    | max    |                        |
| ------------------------------ | ------ | ------ | ---------------------- |
| Uppladdning (POST /api/photos) | 855 ms | 881 ms | 10/10 ok               |
| Health (GET /api/health)       | 372 ms | 777 ms | 8 anrop                |
| processingMs (bildarbetet)     | 54 ms  | 62 ms  |                        |
| apiMs (API:ets totala tid)     | –      | –      | saknas i svaret (före) |

Total tid: 891 ms · kallstarter i svaren: 0
