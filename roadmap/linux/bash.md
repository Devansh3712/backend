bash scripts end with `.sh` and start with a `shebang`. shebang is a combination of `bash #` and `bang !` followed by the bash shell path.

```bash
#!/bin/bash
```

## variables and data types

- assign the value directly
```bash
country=India
```

- assign the value based on the output obtained from a program or command, using command substitution

```bash
same_country=$country
```

## gathering input

- reading the user input and storing it in a variable, using the `read` command
```bash
#!/bin/bash
echo "Enter your name:"
read name
echo "Hello, $name"
```

- reading from a file
```bash
while read line
do
  echo $line
done < input.txt
```

- command line arguments: `$1` denotes the initial argument passed, `$2` denotes the second and so on
```bash
echo "Hello, $1"
```

## displaying output

- writing to file
```bash
echo "Hello world" > output.txt
```
`>` operator overwrites a file if it already has some content.

- appending to the end of a file
```bash
echo "Have a nice day" >> output.txt
```

- redirecting output
```bash
ls > files.txt
```
lists the files in the current directory and writes the output to a file named `files.txt`

## conditional statements
expressions that produce a boolean result, either true or false.

```bash
if [[ condition ]]; then
  statement
elif [[ condition ]]; then
  statement
else
  statement
fi
```

## looping and branching

- **while loop**: checks for a condition and loops until the condition remains true
```bash
i=1
while [[ $i -le 10 ]]; do
  echo "$i"
  (( i += 1 ))
done
```

- **until loop**: checks for a condition and loops until the condition remains false
```bash
i=10
until [[ $i -eq 0 ]]; do
  echo "$i"
  (( i -= 1 ))
done
```

- **for loop**: allows to execute statements for a specific number of times
```bash
for i in {1..10}
do
  echo $i
done
```

## case statement
used to compare a given value against a list of patterns and execute a block of code based on the first pattern that matches

```bash
case expression in
  pattern1)
    statement
    ;;
  pattern2)
    statement
    ;;
  *)
    default statement
    ;;
esac
```
