0.5.0.8
=======
- add support for USB Attached SCSI (UAS) devices
- update of 7-Zip DLL, supported methods are:
  - Brotli v1.0.7
  - Fast LZMA2 v1.0.0
  - Lizard v1.0
  - LZ4 v1.8.3
  - LZ5 v1.5
  - Zstandard v1.3.8
  - and these: Deflate, Deflate64, Bzip2, PPMD, LZMA, LZMA2

0.5.0.7
=======
- fix again problems with opening the Index file
- generate only one backup of Index, delete all other
- update of 7-Zip dll, supported methods are:
  - Brotli v.1.0.1
  - Lizard v1.0
  - LZ4 v1.8.0
  - LZ5 v1.5
  - Zstandard v1.3.2
  - and these: Deflate, Deflate64, Bzip2, PPMD, LZMA, LZMA2

0.5.0.6
=======
- fix problems with german umlaut characters (���)
- generate backups of old index files
- update of 7-Zip dll
  - ZStandard Version 1.1.4
  - LZ4 Version 1.7.5
  - LZ5 Version 1.5

0.5.0.5
=======
- update of 7z.dll
  - additional support of zstd v1.1.3 and lz4 v1.7.5
- binaries are not compressed with upx or mpress

0.5.0.4
=======
- only one binary with support for 32bit and 64bit (VSS, 7-Zip)
- update of 7z.dll to zstd v0.7.2
- added small fix for correct background in the fflabels

0.5.0.3
=======
- update of 7z.dll to version 16.02

0.5.0.2
=======
- update of 7z.dll to version 16.00

0.5.0.1
=======
- made the code compatible with autoit v3.3.14.2 (some array stuff changed)
- writing the Index didn't work correctly some times, fixed now!
- exclamation mark icon in taskbar, if the backup is to old
- improved english translation

0.5.0.0
=======
- ZStandard is the default compressing mode now
- the default value for the complete backups was increased to one year
- fix: the code signing of USB-Backup 0.4.0.9 was not okay :/
- I need to write the help file... :(

0.4.0.9
=======
- update of 7z.dll to version 15.14
- this 7z.dll has ZStd support now ;)
- fix: the ini value ShowUpdateHint was not saved/restored correctly

0.4.0.8
=======
- update of 7z.dll to version 15.06
- new work around for the "wait for nothing loop", problem is solved now!

0.4.0.7
=======
- the default 7za.dll of 7-Zip can't compress with bzip2 or deflate
- I compiled a new 7za.dll with support for bzip2 and deflate and also
  optimized for speed via /Ox and /Ot 
- the 7zg-mini.exe is also optimzed for speed now
- F1 while displaying the Status of Backup didn't work, this is fixed

0.4.0.6
=======
- use 7za.dll instead of the 7z.dll (we are using only 7zip archives...)
- update of 7-Zip to Version 15.05

0.4.0.5
=======
- GetOldestBackup() didn't search for the oldest TimeStamp .. now it does!
- removed registry hack for empty admin passwords, this is bad design...
- use _WinAPI_SendMessageTimeout() instead of ControlClick() - this seems
  to fix the "wait for nothing loop" - which "sometimes" occurred

0.4.0.4
=======
- status page will show the date/time of the last backup
- the english translation is complete now
- fixed some spelling errors in german and english translation

0.4.0.3
=======
- change the current windows power plan for disabling pm features
- improved handling of usb stick events, will just work now ;)
- ShowStatusMessage=1 -> give status of backup via MsgBox()
- new variables for executing commands before / after backup:
  - RunBeforeCmd: run script before backup, usb-backup will wait until script
    is finished
  - RunAfterCmd: run script directly after backup, usb-backup will wait for it

0.4.0.2
=======
- fixed bug for the comments in the exclude files
- fixed update for x64 (new restart code)
- added "-ssc" to the default 7zip options, so folders/files on network
  drives get archied correctly

0.4.0.1
=======
- added internationalization, the english one is not really finished, but
  maybe someone mails me the translation...
- Bugfix: sometimes the backup was done okay, but usb-backup throws a fatal
  error ... this was a very bad fault, so all users must update!
- improved - GetCurrentSticks()

0.3.0.16
========
- 7z.dll unterst�tzt nun deflate, bzip2 usw.

0.3.0.15
========
- neues Feature: MaxFullBackups=X oder 0=disabled
- pr�fen ob Tempdir auf NTFS liegt, wenn ja: dann Index als Stream schreiben
- [Junction] beim Kommentar in den Ausschlusslisten mit rein gemacht
- wenn der Index kaputt ist, wird das Passwort nun jedes mal neu abgefragt
- fix beim Pr�fen auf Updates, sowie Unterst�tzung f�r 64bit
- fix f�r Status, wenn ein Task beendet wurde, mu� das nicht immer
  sofort angezeigt werden... sondern nur, wenn das der aktuelle Task ist!
- ui, Bug bei StringFormatTime() gefixt: %m <> %M
- Logfiles haben nun je Komplettsicherung einen extra Pfad, dieser wird bei
  l�schen des entsprechenden Sicherung auch gel�scht

0.3.0.14
========
- tempor�rer Index wird erstmal nicht mehr versteckt, gab Probleme
- diverse Variablen mit "Const" versehen, damit Sie nicht ge�ndert werden k�nnen

0.3.0.13
========
- tempor�rer Index wird nun ein wenig via NTFS Streams versteckt
- das Dim a[] durch Local a[] ersetzen wieder r�ckg�ngig gemacht
