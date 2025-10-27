# Errores
```bash
http://http.kali.org/kali kali-rolling/main amd64 Contents (deb) File has unexpected size (52315657 != 52314457). Mirror sync in progress? [IP: 104.17.254.239 80] 404 Not Found [IP: 54.39.128.230 80]
Failed to fetch http://http.kali.org/kali/dists/kali-rolling/main/Contents-amd64 404 Not Found [IP: 54.39.128.230 80]
```

* Se crean los archivos 

kali-config/common/includes.chroot/etc/apt/apt.conf.d/99no-contents
config/archives/apt.conf (fuera del chroot)
config/archives/sources.list (fuera del chroot)

* En el build.sh se adiciona

export LB_APT_CONF_FILES="config/archives/apt.conf"
