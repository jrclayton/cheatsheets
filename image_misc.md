
sed replace regex new
```bash
cat file.txt | grep -i "IMG_" | grep -i ".MP4" | sed -E -e 's/[^\/]+$//' | sort | uniq > videos.txt
```

```bash
cat file.txt | grep -i ".AAE" sed -E -e 's/[^\/]+$//' | sort | uniq > trash.txt
```
AAE
.xmp
empty folders and files


Find HEIC folders
```bash
find "`pwd`" -type f -iname "*.HEIC" | sed -E -e 's/[^\/]+$//' | sort | uniq > heic2.txt
```

Find empty folders
```bash
find "`pwd`" -type d -exec bash -c "echo -ne '{}'; ls '{}' | wc -l" \; | awk '$NF==0' > empty.txt
find "`pwd`" -type d -empty > empty.txt
```

Unique
```bash
cat trash.txt | grep -i "/Share" | sed -E -e 's/[^\/]+$//' | sort | uniq > delete.txt
exiftool -json input.jpg > output.JSON
 | awk -F $'\t' '{print $3}'
```

```bash
find . -type d -exec bash -c "echo -ne '{} '; ls '{}' | wc -l" \; | awk '$NF==0'
```
```bash
cat data.txt | grep -i "\.heic" > encode.txt
cat convertir.txt | sort | uniq > encode2.txt 
```
```bash
[^\/]\w+\.heic$
```
---

Solo los que no tengan "-" luego del 3er tab
```bash
cat ~/check.txt | egrep -v '.*\t.*\t.*\t\-'
```

```bash
exiftool \
-r \
-T \
-directory \
-filename \
-Make \
-Model \
-DateTimeOriginal \
-ext JPG \
-ext JPEG \
/DIR \
> ~/check.txt
```


Adobe Caches?
```
~/Library/Application Support/Adobe/Common/PTX/
~/Library/Application Support/Adobe/Common/Team Projects Cache/
~/Library/Application Support/Adobe/Common/Media Cache Files/
~/Library/Application Support/Adobe/Common/Media Cache/
~/Library/Application Support/Adobe/Common/Essential Graphics/
```

Picasa DB Folder
```
~/Library/Application Support/Google/Picasa3
```

Regex
```bash
find . -regex "./[0-9a-fA-F]{8}\-[0-9a-fA-F]{4}\-[0-9a-fA-F]{4}\-[0-9a-fA-F]{4}\-[0-9a-fA-F]{12}\.jpe?g"
```



