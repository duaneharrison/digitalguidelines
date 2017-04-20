---
layout: page
title:  "Web Accessibility Pattern Library"
day: 2
---

# Web Accessibility Pattern Library


## Autocomplete

Autocomplete allows users to complete words in text fields without needing to type them in full.


```sh
&.ui-state-focus, &.ui-state-active {
       a {
         margin: 0;
         color: $cx-white;
         border: 1px dotted transparent;
         +theme('cathay-pacific') {
           background-color: $cx-green-warm;
         }
         +theme('dragon-air') {
           background-color: $ka-red-dark;
         }
       }
     }
```

Components Using this Pattern:

* Flight Search Panel
* Hotel Search Panel
* Package Search Panel
* Flight Timetable
* Inflight Entertainment - Origin/Destination Search


## Button

The button component is useful for committing to an action such as submitting a form.

```sh
<button type="submit" class="button-submit">
    <span class="button-title-small">Search flights</span>
    <span class="button-title-medium">Search</span>
    <span class="button-title-large">Search flights</span>
    <i class="icon icon-arrow-forward" aria-hidden="true" lang="en"></i>
</button>
```
     
```sh
	.book-trip .button-submit{
    border:1px solid transparent;
    -webkit-border-radius:2px;
    -moz-border-radius:2px;
    border-radius:2px;
    background-color:#c2262e;
    background:linear-gradient(0deg,#a62128 0,#cb464d 100%);
    -moz-box-shadow:0 1px 0 0 #c6c2c1;
    -webkit-box-shadow:0 1px 0 0 #c6c2c1;
    box-shadow:0 1px 0 0 #c6c2c1;
    color:#fff;
    width:100%;
    padding:.8em 0;
}
```