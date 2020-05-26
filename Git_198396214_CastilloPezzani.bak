#!r6rs

;Aqui se importa r6rs
(import (rnrs lists (6))
        (rnrs base (6))
        (rnrs io simple (6))
        (rnrs r5rs (6)))


;########################################################################################


;TDA Archivo
; nombre
; lista contenido

;Representacion
; (nombre (list contenido))


;TDA Zonas
; index
; local repository
; remote repository

;Representacion
; (localRepo remoteRepo workSpace)



;########################################################################################


;########################################################################################
; Funcion Git

(define git




)

;########################################################################################


;########################################################################################
; Funcion Pull

(define pull
  

  
)


;########################################################################################


;########################################################################################
; Funcion Add

(define (add)
  (lambda (archivos)
    (lambda (zonas)
      #t
      )
    )
)


;########################################################################################


;########################################################################################
; Funcion Unir

(define (unir lista1 lista2)
   (if (null? lista2)
      (list)
      (if (null? lista1)
          (cons (car lista2) (unir lista1 (cdr lista2)))
          (cons (car lista1) (unir (cdr lista1) lista2))
          )
      )
)


;########################################################################################


;########################################################################################
; Funcion Commit

(define commit
  

  
)


;########################################################################################


;########################################################################################
; Funcion Push

(define push
  

  
)


;########################################################################################


;########################################################################################
; Funcion Zonas -> String

(define zonasToString
  

  
)


;########################################################################################


;########################################################################################
; Funcion ObtenerXpos

(define (obtenerXpos numero lista)
  (if (> numero (length lista))
      #f
      (if (= numero 1)
          (car lista)
          (obtenerXpos (- numero 1) (cdr lista))
          )
      )
)


;########################################################################################


;########################################################################################
; Funcion Setter de contenido

(define (setCont anterior stringNuevo)
  (list (obtenerXpos 1 anterior) stringNuevo)
)


;########################################################################################


;########################################################################################
; Funcion Getter de contenido

(define (getCont archivo)
  (car (obtenerXpos 2 archivo))
)


;########################################################################################


;########################################################################################
; Funcion Comparar Contenido
; Recibe dos strings que pueden ser manejados como listas y comparar dato a dato

(define (compararContenido listStringAnterior listStringNuevo)
  (if (and (null? (car listStringAnterior)) (null? (car listStringNuevo)) )
      #t
      (if (equal? (car listStringAnterior) (car listStringNuevo))
          (compararContenido (cdr listStringAnterior) (cdr listStringNuevo))
          #f
          )
      )
)


;########################################################################################


;########################################################################################
; Funcion Comparar

(define (comparar anterior nuevo)
  (if (equal? (obtenerXpos 1 anterior) (obtenerXpos 1 nuevo))
      (if (compararContenido (string->list (getCont anterior)) (string->list (getCont nuevo)))
          anterior
          (setCont anterior (getCont nuevo))
          )
      #f
      )
)


;########################################################################################




(define test1 (list "archivo1.txt" (list "Hola mundo")))
(define test2 (list "archivo2.txt" (list "Hello World")))

(define test3 (list "Hola mundo"))
(define test4 (list "Hello World"))

(comparar test1 test2)

