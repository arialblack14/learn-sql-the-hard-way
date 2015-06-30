##Learn SQL the Hard Way

####Introduction

I am following [theodinproject](http://http://www.theodinproject.com/web-development-101/databases?ref=lnav) as part of my attempt to better understand the various web development assets in order to be able to make web (or mobile) apps.

So, instead of going through the Stanford class "Introduction to Databases" (which i had completed when it was made available) i decided to do [learn SQL the Hard Way](http://sql.learncodethehardway.org/book/).

####Debugging LSQLTHW

The author, while writing this wonderful book, has not explained some stuff making me rub my head, when trying to run his code. So here is my fixes in case someone else is facing similar errors. Excuse any misuse of the English language.

######Ex1

In order to make a .db file, you have to create a .sql file and then do :

```
sqlite3 ex1.db < ex1.sql
```
which will create the database.
