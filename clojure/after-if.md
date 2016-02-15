### Multiple Statements After If

Clojure's (if) takes two arguments. If you want two things to happen when your condition is true, you can wrap these things in a (do):

```(if (should-go-left args)
  (do
    (println "Going left!")
    (go-left args))
  (do
    (println "Going right!")
	(go-right args)))```
