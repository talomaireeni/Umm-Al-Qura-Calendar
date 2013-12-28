Umm Al-Qura Calendar
====================

A javascript library for converting Gregorian date to Hijri date (Umm Al-Qura calculation). This library was adapted from [Robert Harry van Gent work](http://www.staff.science.uu.nl/~gent0113/islam/ummalqura_converter.htm). I modified the code a bit to make it stand alone and modular.

What is Hijri Calendar
======================

Well, if you do not know what is Hijri Calendar already then this repo may be not for you. If you insist, it is used by more than a billion Muslims around the world to determine the main days of observance in the Islamic religious year. Although in daily life the Western (Gregorian) calendar is now generally followed, the Islamic lunar calendar has since the days of the prophet Muhammad regulated the key days in the Islamic year such as the start and end (‛Īd al-Fitr) of the month of fasting (Ramadān) and the Day of Sacrifice (‛Īd al-Adhā on 10 Dhū ’l-Hijja) during the annual pilgrimage (hajj) at Mecca. For more info, [check out this article](http://en.wikipedia.org/wiki/Islamic_calendar).

What is Umm Al-Qura Calendar
============================

It is the official sighting method to determine the beginning and length of each month of the Hijri calendar in Saudi Arabia. It is one method for calculation based on history and other complex stuff. If you live or develop for something to be used in Saudi Arabia, this library will save your time.

What is inside
==============

A single stand alone javascript file. It can be used in any javascript project: Web, Node.js, Appcelerator, PhoneGap, etc. It contains both historical data and calculation algorithms. This code is based on the Umm al-Qura calendar and is valid from 1356 AH (14 March 1937 CE) to 1500 AH (16 November 2077 CE). Outside this interval, the converter will give erroneous results.

Usage
=====
After including the file "UQCal.js", there are two ways to use UQCal:
Basic Usage:
-------------------
```
var cal = new UQCal(); // assuming today is 28th of December 2013.
var HijriDate = cal.convert();
console.log(HijriDate);
/*
THE RESULT:
{Gday: 28,Gmonth: 12,Gyear: 2013,Hday: 25,Hlength: 29,Hmonth: 2,Hyear: 1435,ilunnum: 17210,julday: 2456655,wkday: 6}
*/
```

Convert a Specific Date:
-------------------------------
```
var cal = new UQCal('2013-12-20');
var HijriDate = cal.convert();
console.log(HijriDate);
/*
THE RESULT:
{Gday: 20,Gmonth: 12,Gyear: 2013,Hday: 17,Hlength: 29,Hmonth: 2,Hyear: 1435,ilunnum: 17210,julday: 2456647,wkday: 5}
*/
```

Documentation
============
The library is simple and self explanatory. The following shows everything you need to know:
UQCal Object Construction:
-------------
* `var cal = new UQCal(date);` `date` is optional, Defaults to Today's date.

Date Conversion:
-------------------------
* `cal.convert();` where the actual conversion happen.

Output:
------

<table>
  <tr>
    <th>Name</th><th>Type</th><th>Description</th>
  </tr>
 <tr>
    <td>Gday</td><td>Integer</td><td>Gregorian day.</td>
  </tr>
 <tr>
    <td>Gmonth</td><td>Integer</td><td>Gregorian month.</td>
  </tr>
 <tr>
    <td>Gyear</td><td>Integer</td><td>Gregorian year.</td>
  </tr>
 <tr>
    <td>Hday</td><td>Integer</td><td>Hijri day.</td>
  </tr>
 <tr>
    <td>Hmonth</td><td>Integer</td><td>Hijri month.</td>
  </tr>
 <tr>
    <td>Hyear</td><td>Integer</td><td>Hijri year.</td>
  </tr>
 <tr>
    <td>Hlength</td><td>Integer</td><td>The length of the Hijri month, 29 or 30.</td>
  </tr>
 <tr>
    <td>ilunnum</td><td>Integer</td><td>I have no idea :(</td>
  </tr>
 <tr>
    <td>julday</td><td>Integer</td><td>Chronological offset between Julian and Gregorian calendar.</td>
  </tr>
 <tr>
    <td>wkday</td><td>Integer</td><td>Number of day in the week, Monday being #1.</td>
  </tr>
</table>



