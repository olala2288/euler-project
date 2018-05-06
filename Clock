(setq st "")
(setq inc t)
(setq dec nil)
(setq index 1)
(setq sIndex 0)


(defun makeSeq()
	(loop for i from 1 to 1000

		do(
			when inc 
		    (setq st (concatenate 'string st (write-to-string index)))
			(setq index (+ index 1))
			

			(when (> index 4)
				(setq inc nil)
				(setq dec t)
				(setq index 3)
				)
			)

		do (
			
			when dec 
			(setq st (concatenate 'string st (write-to-string index)))
			(setq index (- index 1))
			

			(when (<= index 0)
				(setq dec nil)
				(setq inc t)
				(setq index 2)
				)

			)
		)
	st
	)

(defun cutString (str cutIndex)
	(setq str (subseq str cutIndex) return str)
	)

(defun concatAns (answer mChar)

	(setq answer (concatenate 'string ans (write-to-string mChar)) return answer)
	)


(defun findSeq(num)
	(setq temp (makeSeq))
	(setq ans "")
	(loop for x from 1 to num 
			do(setq sIndex 0)
			do(setq ch (char temp sIndex))
			do(setq n (digit-char-p ch))
			
			do( when (/= x num )
				(setq ans "")
				
				(when ( = n x)
				(setq temp (cutString temp (+ sIndex 1)))
				)


				(when (/= n x)

					(setq sm n)
					(loop while(<= sm x)
						do(setq ans (concatAns ans (digit-char-p ch)))
						do(setq sIndex (+ sIndex  1))
						do(setq ch (char temp sIndex))
						do(setq sm (+ sm (digit-char-p ch)))
						do(when (= sm x)
							(setq ans (concatAns ans (digit-char-p ch)))
							(setq temp (cutString temp (+ sIndex 1)))
							
							)
						)

					)

				)

			do (
				when (= x num)
				(setq ans "")
				(when (= n num)
					(setq ans (concatAns ans n))
					)

				(when (/= n x)
					(setq sm n)
					(loop while(< sm x)
						do(setq ans (concatAns ans (digit-char-p ch)))
						do(setq sIndex (+ sIndex 1))
						do(setq ch (char temp sIndex))
						do(setq sm (+ sm (digit-char-p ch)))
						do(when (= sm x)
							(setq ans (concatAns ans (digit-char-p ch)))
							(setq temp (cutString temp (+ sIndex 1)))
							)
						)

					)

				)

		)
	ans
	)


(defun S(n)
	(setq sm 0)
	(loop for i from 1 to n 

		do(
			setq sm (+ sm (parse-integer (findSeq i)))

			)

		)
	sm
	)

(print (S 11))