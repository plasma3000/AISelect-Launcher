# AISelect-Launcher
Launch AISelect on any windows

ENG

This exe launches AISelect on any windows.
AISelect must be installed first. Install here -> https://apps.microsoft.com/detail/9PM11FHJQLZ4
Windows defender might detected this file as a virus. This can happen to any batch file that has been converted to exe.

KOR

이 파일은 AI샐랙트를 모든 윈도우에서 실행시킵니다.
AI셀렉트가 먼저 깔려있어야 합니다. 여기서 다운받으세요 -> https://apps.microsoft.com/detail/9PM11FHJQLZ4
윈도우 디펜더가 이 파일을 바이러스라고 여길 수 있습니다. 이는 exe로 변환한 배치파일이라면 일어날 수 있습니다.

CODE

set "params=%*" && cd /d "%~dp0" && pushd "%~dp0" && ( if exist "%temp%\getadmin.vbs" del "%temp%\getadmin.vbs" ) && fsutil dirty query %systemdrive% 1>nul 2>nul || (  echo Set UAC = CreateObject^("Shell.Application"^) : UAC.ShellExecute "cmd.exe", "/k cd ""%~sdp0"" && %~s0 %params%", "", "runas", 1 >> "%temp%\getadmin.vbs" && "%temp%\getadmin.vbs" && exit /B )

:: Set the system product name and system manufacturer to Galaxy Book 5 Pro
reg add "HKLM\HARDWARE\DESCRIPTION\System\BIOS" /v SystemProductName /t REG_SZ /d "NT960XHA-KD72G" /f
reg add "HKLM\HARDWARE\DESCRIPTION\System\BIOS" /v SystemManufacturer /t REG_SZ /d "Samsung" /f

:: Goto directory
cd C:\Program Files\Samsung\AI Select Service > nul

:: Start AIselect startup Batch file
startup.bat > nul

:: Exit
exit
