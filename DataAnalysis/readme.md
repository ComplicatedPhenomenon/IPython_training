How to read in little by little?
* `f.read()` This reads from the file based on the number of size bytes.
* `f.readline(size = 5)` This reads at most size number of characters from the line.
* `f.readlines(size = 5)` This reads the remaining lines from the file object and returns them as a list.

```sh
%cat dog_breeds.txt
Pug
Jack Russell Terrier
English Springer Spaniel
German Shepherd
Staffordshire Bull Terrier
Cavalier King Charles Spaniel
Golden Retriever
West Highland White Terrier
Boxer
Border Terrier
```
```py
with open('dog_breeds.txt', 'r') as reader:
    # Read & print the first 5 characters of the line 5 times
    print(reader.readline(5))
    print(reader.readline(5))
    print(reader.readline(5))
    print(reader.readline(5))
```

```
Pug

Jack
Russe
ll Te
```
