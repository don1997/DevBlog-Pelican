Title: Factorials in Scheme using linear recursiona and iterative approach
Date: 2010-12-03 10:20
Category: SICP 

Here is an example of a factorial program in racket

	:::racket
	;;;helpful template https://stackoverflow.com/questions/36971743/trying-to-create-a-recursive-function-in-scheme

	;;biggest problem was i forgot to do x - 1 in func call
	;;;Using if (aka "SICP style")
	(provide pascal)
	(define (pascal x)
	 (if (zero? x)
	  1
	  (* 2 (pascal (- x 1)))))


	;;Using cond (aka "Little schemer style")
	(provide pascal2)
	(define pascal2
	 (λ (x)
	  (cond
	   ((= x 0) 1)
	   ((= x 1) 2)
	   (else
	    (* 2 (pascal (- x 1)))))))



