I made Codex Mod Workshop, a live website with a Beat Saber map generator, lightshow fixer, preview tools, and more. I’m also putting the updated version into a GitHub repository so I can keep improving it and track changes.
https://close-blush-welndhrlqd.edgeone.app/mod-generator-home.html
or your to lazy to install the exe use this in command prompt    @echo off
setlocal

set ZIP_FILE=codex-projects-monorepo.zip
set INSTALL_DIR=%USERPROFILE%\Documents\CodexProjectsMonorepo

echo Installing Codex Projects Monorepo...
echo.

if not exist "%ZIP_FILE%" (
  echo Package zip not found: %ZIP_FILE%
  pause
  exit /b 1
)

if not exist "%INSTALL_DIR%" (
  mkdir "%INSTALL_DIR%"
)

powershell -Command "Expand-Archive -LiteralPath '%ZIP_FILE%' -DestinationPath '%INSTALL_DIR%' -Force"

if errorlevel 1 (
  echo.
  echo Install failed.
  pause
  exit /b 1
)

echo.
echo Install complete.
echo Installed to: %INSTALL_DIR%
pause
