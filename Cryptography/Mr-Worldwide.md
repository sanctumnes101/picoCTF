## Description

> A musician left us a message. What's it mean?


## Hints

> None
 

## Approach & Solution

If we open the message, we get the following text:

```
picoCTF{(35.028309, 135.753082)(46.469391, 30.740883)(39.758949, -84.191605)(41.015137, 28.979530)(24.466667, 54.366669)(3.140853, 101.693207)_(9.005401, 38.763611)(-3.989038, -79.203560)(52.377956, 4.897070)(41.085651, -73.858467)(57.790001, -152.407227)(31.205753, 29.924526)}

```

These look like GPS coordinates. Let's use [Google Maps](https://www.google.com/maps) to get the locations of these coordinates.

Locations in order using google maps:
```
Nakanocho, Kamigyo Ward, Kyoto, 602-0958, Japan
Odesa, Odessa Oblast, Ukraine, 65000
Dayton, OH 45402, United States
Hoca Paşa, 34110 Fatih/İstanbul, Turkey
Hazza' Bin Zayed the First St - Al Manhal - Abu Dhabi - United Arab Emirates
50480 Kuala Lumpur, Federal Territory of Kuala Lumpur, Malaysia
_
Kirkos, Addis Ababa, Ethiopia
Av Nueva Loja, Loja, Ecuador
Martelaarsgracht 5, 1012 TN Amsterdam, Netherlands
188 vida activa, Sleepy Hollow, NY 10591, United States
Kodiak, AK 99615, United States
Faculty Of Engineering, Al Azaritah WA Ash Shatebi, Qism Bab Sharqi, Alexandria Governorate, Egypt
```

These are full addresses, let's get the city and country:

+ Kyoto, Japan
+ Odessa, Ukraine
+ Dayton, US
+ Istanbul, Turkey
+ Abu Dhabi, UAE
+ Kuala Lumpur, Malaysia
+ _
+ Addis Ababa, Ethiopia
+ Loja Loja, Ecuador
+ Amesterdam, Netherlands
+ Sleepy Hollow, US
+ Kodiak, US
+ Alexandria Governorate, Egypt

Now let's form the flag using the first letters of either the cities or the countries. We have 2 possibilities:

1. JUUTUM_EENUUE (which doesn't mean anything)
2. KODIAK_ALASKA (which obviously mean something!)


## Final Answer

`picoCTF{KODIAK_ALASKA}`
