

//	IF (<ACT.TAG0.SKILLBOOST1>)
//		SRC.addcliloc 1063468,<SERV.SKILL.<ACT.TAG0.SKILLBOOST1>.KEY>,<EVAL <ACT.TAG0.SKILLBOOST1AMT>/10>
//	ENDIF
//	IF (<ACT.TAG0.SKILLBOOST2>)
//		SRC.addcliloc 1060455,<SERV.SKILL.<ACT.TAG0.SKILLBOOST2>.KEY>,<EVAL <ACT.TAG0.SKILLBOOST2AMT>/10>
//	ENDIF

	IF (<ACT.TAG0.DEXINCREASE>)
		SRC.ADDCLILOC 1060409,<EVAL <ACT.TAG0.DEXINCREASE>>
	endif
	IF (<ACT.TAG0.STRINCREASE>)
		SRC.ADDCLILOC 1060485,<EVAL <ACT.TAG0.STRINCREASE>>
	endif
	IF (<ACT.TAG0.INTINCREASE>)
		SRC.ADDCLILOC 1060432,<EVAL <ACT.TAG0.INTINCREASE>>
	endif
	IF (<ACT.TAG0.MODHITS>)
		SRC.ADDCLILOC 1060431,<EVAL <ACT.TAG0.MODHITS>>
	endif
	IF (<ACT.TAG0.MODMANA>)
		SRC.ADDCLILOC 1060439,<EVAL <ACT.TAG0.MODMANA>>
	endif
	IF (<ACT.TAG0.MODSTAM>)
		SRC.ADDCLILOC 1060484,<EVAL <ACT.TAG0.MODSTAM>>
	endif

	IF (<ACT.TYPE>==T_ARMOR) || (<ACT.TYPE>==T_SHIELD) || (<ACT.TYPE>==T_ARMOR_LEATHER) || (<ACT.TYPE>==T_CLOTHING)
		IF (<ACT.TAG0.DAMAGERETURN>)
			SRC.ADDCLILOC 1060442,<EVAL <ACT.TAG0.DAMAGERETURN>>
		endif
		IF (<ACT.TAG0.HITCHANCEDECREASE>)
			SRC.ADDCLILOC 1060408,<EVAL <ACT.TAG0.HITCHANCEDECREASE>>
		endif
		IF (<SRC.ARMSLORE> > 100)
			SRC.ADDCLILOC 1060847,Armor,<EVAL <ACT.MODAR>+<ACT.ARMOR>>
			IF (<ACT.TAG0.COLDRESIST>)
				SRC.ADDCLILOC 1060445,<EVAL <ACT.TAG0.COLDRESIST>>
			ENDIF
			IF (<ACT.TAG0.ENERGYRESIST>)
				SRC.ADDCLILOC 1060446,<EVAL <ACT.TAG0.ENERGYRESIST>>
			ENDIF
			IF (<ACT.TAG0.FIRERESIST>)
				SRC.ADDCLILOC 1060447,<EVAL <ACT.TAG0.FIRERESIST>>
			ENDIF
			IF (<ACT.TAG0.POISONRESIST>)
				SRC.ADDCLILOC 1060449,<EVAL <ACT.TAG0.POISONRESIST>>
			ENDIF
		ENDIF
	ELIF (STRMATCH(*t_weapon*,<ACT.TYPE>))
		IF (<SRC.ARMSLORE> > 100)
			SRC.ADDCLILOC 1061167,<ACT.SPEED>
		ENDIF
		IF (<SRC.ARMSLORE> > 100)
			SRC.ADDCLILOC 1061168,<ACT.DAM>
		ENDIF
		IF (<SRC.ARMSLORE> > 100) && (<ACT.RANGE> > 1)
			SRC.ADDCLILOC 1061169,<ACT.RANGE>
		ENDIF


	endif





GumpMaker v0.2
(c)2001-2001
written by Kerem 'wastiee' HADIMLI

wastiee@candledreams.net

Check out
http://www.candledreams.net/wastiee/gumpmaker.html
for new version!


* Well, this program is alpha version, and the only reason of releasing this
program to public is to make myself continue GumpMaker :)

* Also, this program is freeware :)

* There is not much to say about the program, Load/Save isn't implemented
yet, but you can export your gump to an ini file if you want, it will export
in uo-client style, but you will have to modify the ini file, based on the
emulator you're using.

* The program needs some client-side files in the same folder in order to
work. When you run it, it will say which files it needs, and you should copy the
required file to the same directory where GumpMaker.exe is. Another solution is
to put GumpMaker.exe in Ultima Online directory.

* Don't forget this is alpha version, and is incomplete. There are a lot of
thoughts, a lot of stuff needs to be done, but the main thing is working
properly. I think I need some morale to continue this project (it was idle for
the last few months), that's why i decided to release it.

* I hope you like it, don't hesitate to send me an email if you like it :)

Thanks to;
+ Alazane, for making InsideUO, and publishing Ultima Online client-side
file details on his website
+ Odion, for testing GumpMaker, and making me continue this project :)


27/06/2002 -wastiee