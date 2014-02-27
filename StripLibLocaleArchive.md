# Strip (Reduce) Locale Archive in /usr/lib/locale/
-------------------------------------------------

Execute the following commands in numbers below:

```bash
1) localedef --list-archive | grep -v -i ^en | xargs localedef --delete-from-archive
```
where en can be replaced with the one you wish to keep

```bash
2) build-locale-archive
```
 If you encounter an error that says '/usr/sbin/build-locale-archive: cannot read archive header', go to step 2a) and repeat step 2

```bash
   2a) mv /usr/lib/locale/locale-archive /usr/lib/locale/locale-archive.tmpl
```





