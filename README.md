#java-crontab-expression#

Java library for parsing **crontab expressions** (actually, a subset of them) and returning dates or milliseconds
relative to time references. Currently there is just one class which objects are created by passing the crontab
expression as its only parameter. It parses and "compiles" the expression upon creation. You may then work with
it by passing a time reference.

**IMPORTANT: _It only looks for matches within the same year and the year before or after._**

##Current functionality##

```
[constructor] FixedPeriodCron(String crontabExpression)
```
```
Calendar getClosestDateBeforeOrSame(Calendar timeReference)
```
```
Calendar getClosestDateAfter(Calendar timeReference)
```
```
Long nextMatchInMillis(Calendar timeReference)
```
```
Long periodInMillis(Calendar timeReference)
```
...and its field getters.
