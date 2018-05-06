(defun checkfriends (a b)

	(setq target (write-to-string a))
	(setq temp (write-to-string b))

	(loop for i from 0 below (length target)
		for ch = (char target i)
		when(find ch temp :test #'eql)
		return t
		)
	)

(setq sm 0)

(defun friendNumber (n)
	(setq n (- n 1))
	(loop for x from 1 to n
		do(loop for y from (+ x 1) to n 
		do(when(checkfriends x y)
			(setq sm (+ sm 1))
			)
		)
	)
	(print sm)
	)

(friendNumber 100)
