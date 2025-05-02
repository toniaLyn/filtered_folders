FROM kalilinux/kali-rolling

COPY requirements.txt .
RUN pip3 install -r requirements.txt

RUN net user /add ctf

COPY UserRights.ps1 /
COPY AllowSymlinks.ps1 /
RUN powershell.exe -File C:/AllowSymlinks.ps1
 
COPY executables/*.exe /exes/

ADD app/ /app
WORKDIR /app
ENTRYPOINT waitress-serve --listen=*:2753 app:app