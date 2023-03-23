------------------------------------------------------

	WARSZAWSKA WYZSZA SZKOLA INFORMATYKI

	        PRACA DYPLOMOWA 
	     WYZSZE STUDIA ZAWODOWE


	       Maciej GRZESZCZUK
			Numer albumu  2229

	Wieloprocesowy system operacyjny 
	 dla komputerów Atari XL/XE




			Promotor:
			  mgr inz. Dariusz MAJKA


		   WARSZAWA 2006

------------------------------------------------------


Zawartosc plyty:
----------------

README.TXT	- niniejszy plik

emu/Atari800Win PLus 4.0.exe	- wersja instalacyjna
				  emulatora Atari
emu/xf25.zip			- pakiet ROMow Atari

img/XEUX.atr	- obraz dyskietki z systemem XEUX.
		  uruchamia sie automatycznie (boot) i
		  zawiera podstawowe aplikacje.
img/SRC.atr	- obraz dyskietki ze zrodlami systemu
		  w formacie asemblera MAE.
img/UTIL.atr	- obraz dyskietki (boot) z programami
		  narzedziowymi uzytymi w projekcie,
		  w tym tez asembler MAE

src/		- zrodla systemu w formacie plikow PC

doc/		- pelen tekst pracy w formacie MS Word

pdf/		- pelen tekst pracy w formacie PDF


Instalacja emulatora:
---------------------

Aby zainstalowac emulator, nalezy z poziomu Windows
uruchomic plik instalatora (Atari800Win PLus 4.0.exe),
a nastepnie postepowac zgodnie z zaleceniami na
ekranie. Przed pierwszym uruchomieniem nalezy
rozpakowac zawartosc pliku XF25.ZIP. Po uruchomieniu
emulatora powinnismy wskazac miejsce do ktorego
rozpakowano plik ZIP jako lokalizacje plikow
ATARIBAS.ROM, ATARIOSB.ROM oraz ATARIXL.ROM

Nastepnie nalezy skonfigurowac podstawowe parametry
zgodnie z ponizszymi zaleceniami:

  Atari -> Machine Type -> XL/XE
  Atari -> Memory Size  -> 128kB
  Atari -> Video System -> PAL
  Atari -> Options      -> Disable BASIC

Aby podlaczyc obrazy dyskietek, nalezy wykorzystac
skróty klawiszowe ALT plus numer napedu, który chcemy
symulowac. Naped, z którego nastepuje rozruch systemu
(boot), to naped pierwszy


Uruchamianie systemu:
---------------------

Po uruchomieniu emulatora nalezy podlaczyc obraz
dyskietki img/XEUX.atr jako dysk nr 1 (ALT+1),
a nastepnie wykonac zimny start komputera, wciskajac
klawisze SHIFT+F5. System uruchomi sie automatycznie.

