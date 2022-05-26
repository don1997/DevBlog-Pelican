Title: SICP Exercise 1.13
Date: 2010-12-03 10:30
Category: SICP 

	:::racket
	(provide pascal)
	(define (pascal x)
	 (if (zero? x)
	 1
	 (* 2 (pascal (- x 1)))))


		;;Using cond (aka "Little schemer style")
		(provide pascal2)
		(define pascal2
		  (lambda (x)
		    (cond
		      ((= x 0) 1)
		      ((= x 1) 2)
		      (else
			(* 2 (pascal (- x 1)))))))


$e=mc^2$
