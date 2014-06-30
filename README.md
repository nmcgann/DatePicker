# Lightweight javascript datepicker

![Lightweight javascript datepicker](http://remi-grumeau.github.io/DatePicker/images/preview.png "Javascript DatePicker")

This script is a modern browser automatic date picker solution. 
No third-party library dependency, IE support is IE8+.


# How to use
### Simple usage
For a given id attribute of 'birthday', you should have
- an input text with id equal to 'birthday'
- an onclick event on it to open datepicker

```html
<input 
	type="text" 
	name="date_button" 
	id="date_button" 
	value="2011-06-02" 
	onclick="DP.open('date_button','date_button')"
>
```

### Positionning
You can specify a second parameter to specify the datepicker position. If empty, datepicker use the first parameter (aka element ID value) to get its position.
It can be an element ID value, a DOM element or a X,Y array.

```html
<input 
	type="text" 
	name="date_button" 
	id="date_button" 
	value="2011-06-02" 
	onclick="DP.open('date_button','date_button')"
>

<input 
	type="text" 
	name="date_button" 
	id="date_button" 
	value="2011-06-02" 
	onclick="DP.open('date_button', myDomElement)"
>

<input
	type="text"
	name="date_button"
	id="date_button"
	value="2011-06-02"
	onclick="DP.open('date_button', [10,40])"
>
```


### On multiple selects
For a given id attribute of 'birthday', you should have
- 3 selects with ids 'birthday_day', 'birthday_month' & 'birthday_year'.
- an hidden input text with id equal to 'birthday'

```html
<select
	name="date_select1_day"
	id="date_select1_day"
	size="1"
	onblur="DP.update('date_select1')"
>
	...
</select>
			
<select
	name="date_select1_month"
	id="date_select1_month"
	size="1"
	onblur="DP.update('date_select1')"
>
	...
</select>

<select
	name="date_select1_year"
	id="date_select1_year"
	size="1"
	onblur="DP.update('date_select1')"
>
</select>

<input
	type="hidden"
	name="date_select1"
	id="date_select1"
	value="2011-06-02"
>
<a
	href="javascript:DP.open('date_select1','date_select1_dp')"
	id="date_select1_dp"
><img src="datepicker_cal.gif"></a>
```

Please note that in this case, it might be a good idea to add onblur events on select to update the hidden input value when a select value changes.


## Want to contribute
Any contribution is always welcome.
As an example, Responsive CSS and multilingual support would be pretty nice contributions :)

## Special thanks
Thanks to [DtTvB's work](http://javascriptkit.com/script/script2/dyndateselector.shtml), DatePicker really start as a cleanup of it.
