# autohot-test
Sample autohotkey script
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

::btw::By the way ; Replaces "btw" with "By the way" as soon as you press an EndChar.
:*:btw::By the way ; Replaces "btw" with "By the way" without needing an EndChar

^n:: ; Ctrl & n Hotkey
	run, notepad.exe
; Run the program notepad.exe when you press Ctrl & n
Return
; This ends the hotkey. The code below this will not get triggered.

^b::
;Ctrl & b Hotkey
	send, {ctrl down}c{ctrl up}
; Copies the selected text. ^c could be used as well, but this method is more secure.
	SendInput, [b]{ctrl down}v{ctrl up}[/b] ; Wraps the selected text in bbcode (forum) Bold tags.
Return
; This ends the hotkey. The code below this point will not get triggered.
