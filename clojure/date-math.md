### Date Math

If you need to know if a date falls within the last 15 minutes, you can do this easily using the `clj-time` library:

```(time/minus (time/now) (time/minutes 15))```
