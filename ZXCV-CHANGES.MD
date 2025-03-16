Originally tested on 4.3.9 fork from repslet/nightwalker
copy pasted the changes in the ToMattBan/nightwalker fork since they had a repo updated for v5.+
Seems to all still work the same in v5.0.3

I am not a coder, all changes made by googling and fiddling around then seeing what worked
In an acceptable state for my use case, will not be making further changes

Note: Did not know GitHub showed extact changed so cleanly when I first made this file. Which is why I tracking exact code being changed in case I needed to look back on it

all changes made in the following file
nightwalker.css

located at nightwalker-zxcv\private\css\nightwalker.css

1.	Added --color-Yellow: #d1c52a;
		
	Changed
-----------------------------------------------	
			#Filters {
    background: var(--color-Dark) !important;
    color: var(--color-White);
}

a {
    color: var(--color-White) !important;
}

----------------------------------------------
	to
----------------------------------------------	
		#Filters {
    background: var(--color-Dark) !important;
    color: var(--color-White);
}

a {
    color: var(--color-Yellow) !important;
}

-----------------------------------------------
	This made the hyperlinks yellow to stand out more
		

In the /* ICONS IN LEFT SIDEBAR/FILTERLIST* section

2.


ul.filterList a {
    display: inline;

	
	changed to 


ul.filterList a {
    display: block;


	This makes the entire line clickable on the Left Sidebar
	But makes the filters be split out into 2 lines. 1 with the unclickable custom icon and 1 with the clickable text
	This is band-aid fixed with the next change.




3. Commented out the Custom Icons "content:" lines in all the *_filter:before* sections
	
	
4. Added the original icons back by making the following change in all the *_filter>a img* sections

		
		display: none;
	to
		display: inline-block;
	

	
5. Added --color-BlueSelected: #3c5f96;
	Made the filters and dynamic tables these colors instead of --color-GreySelected to stand out more
	
	
	.dynamicTable tr.selected {
    background: var(--color-GreySelected) !important;
}

	
	and 
	
	
	ul.filterList li:hover,
.selectedFilter {
    background: var(--color-GreySelected) !important;
}


	to


	.dynamicTable tr.selected {
    background: var(--color-BlueSelected) !important;
}

	
	and 
	
	
	ul.filterList li:hover,
.selectedFilter {
    background: var(--color-BlueSelected) !important;
}

