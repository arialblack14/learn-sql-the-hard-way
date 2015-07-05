##Learn SQL the Hard Way

####Introduction

I am following [theodinproject](http://http://www.theodinproject.com/web-development-101/databases?ref=lnav) as part of my attempt to better understand the various web development assets in order to be able to make web (or mobile) apps.

So, instead of going through the Stanford class "Introduction to Databases" (which i had completed when it was made available) i decided to do [learn SQL the Hard Way](http://sql.learncodethehardway.org/book/).

####>Debugging LSQLTHW

The author, while writing this wonderful book, has not explained some stuff making me rub my head, when trying to run his code. So here is my fixes in case someone else is facing similar errors. Excuse any misuse of the English language.

######>Ex1

In order to make a .db file, you first have to create the ex1.sql file and then do :
```
sqlite3 ex1.db < ex1.sql
```
which will create the database. If you don't do this you will probably get the error message, 

```
-bash: ex1.sql: No such file or directory.
```

Then if you want to check the contents of your created database, you type in your terminal 
```
sqlite3
```
Now you can interact with it. So, to open ex1.db just do:
```
.open ex1.db
```
######>Ex3

For these examples to run you have to add your data to ex1.db or else you will receive this error message
```
Error: near line 1: table person already exists
Error: near line 8: table pet already exists
Error: near line 16: table person_pet already exists
```
and so on for the others to come.

######>Notes on the exercises
I should also mention that i found [this](http://zetcode.com/db/sqlite/) tutorial on sqlite3 much helpful. This site also has a Ruby-sqlite3 specific [tutorial](http://zetcode.com/db/sqliteruby/).

Definitely use the following, which add headers for your columns and make them look better by sepparating them a bit. 
```
.headers on
.mode column
```
You should also use -echo in order to see which statement produces what result 
```
sqlite3 -echo ex1.db < ex7.sql
```
and combine the above in one sentence like so
```
sqlite3 -header -column -echo ex1.db < ex7.sql
```