# perl

## one-liners

Task 1: Process the file line by line, and return all matches
```perl -ne 'while(/\bc\w+/g){print "$&\n";}' yourfile```

Task 2: Process the file line by line, and return all matching lines
`perl -ne 'print if /\bc\w+/' yourfile`

Task 3: Process the file line by line, and return the first match of each line
`perl -ne 'print "$&\n" if /\bc\w+/' yourfile`

Task 4: Process the file as a block, and return all matches
`perl -0777 -ne 'while(m/\bc\w+/g){print "$&\n";}' yourfile`

Task 5: Process the file as a block, and return the first match
`perl -0777 -ne 'print "$&\n" if /\bc\w+/' yourfile`

Task 6: Process the file as a block, and replace all matches
`perl -0777 -pe 's/\bc\w+/ZAP/g' yourfile`

Task 7: Process the file as a block, and replace the first match
`perl -0777 -pe 's/\bc\w+/ZAP/' yourfile`

Task 8: Process the file line by line, and replace all matches
`perl -pe 's/\bc\w+/ZAP/g' yourfile`

Task 9: Process the file line by line, and replace the first match
`perl -pe 's/\bc\w+/ZAP/' yourfile`

Task 10: Process the file as a block, and split
`perl -0777 -ne 'if(@r=split(m/\bc\w+/,$_)){foreach(@r){print "$_\n";}}' yourfile`

Task 11: Process the file line by line, and split
`perl -ne 'if(@r=split(m/\bc\w+/,$_)){foreach(@r){print "$_\n";}}' yourfile`

http://www.rexegg.com/regex-perl-one-liners.html
