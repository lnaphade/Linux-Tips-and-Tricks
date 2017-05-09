### Awk and Regular Expressions to Filter Text
```
awk -F':' '{ print $1 }' /etc/passwd (. usernames will be print the the first field)

awk '{print NR "- " $1 }' /etc/passwd (To print the first item ($1) and then the second last item )

awk '/localhost/{print}' /etc/hosts  ( awk will match line having localhost in the  /etc/hosts file)


```
