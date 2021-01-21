The script below renames all files under a directory from .hpp to .h
```
for i in $(find . -iname "*.hpp"); do
    git mv "$i" "$(echo $i | rev | cut -d '.' -f 2- | rev).h";
done
```
