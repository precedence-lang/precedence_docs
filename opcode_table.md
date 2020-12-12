0x__|**_0**|**_1**|**_2**|**_3**|**_4**|**_5**|**_6**|**_7**|**_8**|**_9**|**_A**|**_B**|**_C**|**_D**|**_E**|**_F**
:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:
**0_**|add|incr|sub|decr|mult|exp|div|mod|UNUSED|UNUSED|rot2|rot3 up|bit not|bit and|bit or|bit xor
**1_**|dupe top|dupe under|size|set|get|get and set|commit|lt|le|eq|nop|UNUSED|UNUSED|UNUSED|ret|exit
**2_**|gtjmp rel stack|gtjmp abs stack|gtjmp rel 1|gtjmp rel 2|gtjmp rel 3|gtjmp rel 5|gtjmp rel 7|gtjmp rel 10|gtjmp rel -2|gtjmp rel -3|gtjmp rel -5|gtjmp rel -7|gtjmp rel -9|gtjmp rel -12|INF (gtjump rel code)|INF (gtjump abs code)
**3_**|cfjmp rel stack|cfjmp abs stack|cfjmp rel 1|cfjmp rel 2|cfjmp rel 3|cfjmp rel 5|cfjmp rel 7|cfjmp rel 10|cfjmp rel -2|cfjmp rel -3|cfjmp rel -5|cfjmp rel -7|cfjmp rel -9|cfjmp rel -12|INF (cfjump rel code)|INF (cfjump abs code)
**4_**|func id 0|func id 1|func id 2|func id 3|func id 4|func id 5|func id 6|func id 7|func id 8|func id 9|func id 10|func id 11|func id 12|func id 13|func id 14|func id 15
**5_**|func id 16|func id 17|func id 18|func id 19|func id 20|func id 21|func id 22|func id 23|func id 24|func id 25|func id 26|func id 27|func id 28|func id 29|func id 30|func id 31
**6_**|func id 32|func id 33|func id 34|func id 35|func id 36|func id 37|func id 38|func id 39|func id 40|func id 41|func id 42|func id 43|func id 44|func id 45|func id 46|func id 47
**7_**|func id 48|func id 49|func id 50|func id 51|func id 52|func id 53|func id 54|func id 55|func id 56|func id 57|func id 58|func id 59|{func id: 4 bytes}|{func id: 3 bytes}|{func id: 2 bytes}|{func id: 1 byte}
**8_**|0|-1|-2|-3|-4|-5|-6|-7|-8|-9|-10|-11|-12|-13|-14|-1 \* {int: x bytes cont bit}
**9_**|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|{int: x bytes cont bit}
**A_**|shoco len 1|shoco len 2|shoco len 3|shoco len 4|shoco len 5|shoco len 6|shoco len 7|{shoco len: x bytes cont bit}|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)|INF (alphabetic)
**B_**|INF (compressed)|INF (compressed)|INF (compressed)|INF (compressed)|INF (compressed)|INF (compressed)|INF (compressed)|INF (compressed)|INF (custom)|INF (custom)|INF (custom)|INF (custom)|INF (custom)|INF (custom)|INF (custom)|INF (custom)
**C_**|array len 0|array len 1|array len 2|array len 3|array len 4|array len 5|array len 6|array len 7|array len 8|array len 9|array len 10|array len 11|array len 12|array len 13|array len 14|array len 15
**D_**|array len 16|array len 17|array len 18|array len 19|array len 20|array len 21|array len 22|array len 23|array len 24|array len 25|array len 26|array len 27|array len 28|array len 29|array len 30|{array len: x bytes cont bit}
**E_**|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED
**F_**|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED|UNUSED
