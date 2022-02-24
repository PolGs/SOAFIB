# SOAFIB
----Entrega 1------

-Programar 2 Interrupciones
	Posicion 32 IDT para reloj
	Posicion 33 IDT para teclado
	En cada caso saltare al handler adecuado entry.s(clock_handler)
	Para programar IDT programaremos interrupt.c::setZDT -> SetInterruptHandler



Int. Reloj
-32 IDT
-clock_handler(entry.s) -> save_all -> call clock_routine(interrupt.c)


-Programar unica entrada al sistema(syscalls)
	3.8 -> no hay que implementar

	Programar Write() -> wrapper.S
	-Hacer el paso de parametros a registro (pila a nbz,ncz...)
	-Hacer la llamda a l sistema
	-sysenter -> permite cambiar el modo de privilegios(a nv. 0) utilizando los registros MSR -> wrmsr (EAX-donde escrivo, ECX- donde
	-Handler llamadas al sistema(dociumento, entry.S)
	-sys.c -> sys.write(){}


