Flexo
=====

##A nice first attempt at a responsive grid but the system falls flat when trying to calculate different column widths.

Flexo is a mobile-first responsive grid designed to give you a helping hand developing responsive sites. 

Flexo has been designed with simplicity in mind. A five column grid with a sticky footer that scales beautifully up as you go from mobile to desktop. There are multiple column combinations available and columns can also easily be nested.

##Getting started

To create a full height page with a sticky footer requires only the following markup.

    <div class="page">
        <!-- Page content goes here -->
    </div>
    <div class="page-footer">
        <!-- Page footer content goes here -->
    </div>

In IE7 and IE8 and Firefox prior to version 17 pages with content that does not fill the full height of the page will not behave correctly and will add the height of the footer to the page height.

If support for these browsers is required then this alternate markup will work.

    <div class="page no-box">
        <!-- Page content goes here -->
        <div class="page-push">
        <!-- Pushes the footer down -->
        </div>
    </div>
    <div class="page-footer">
        <!-- Page footer content goes here -->
    </div>

##The grid

Flexo will default to **1140px** on Internet Explorer versions 7 and 8 and will scale up to the same width in modern browsers. Changing that value is as simple as overriding one property `.container` in **flexo.css** and **flexo-legacy.css**

The width can also be fixed by adding the class `.flexo-fixed` to the body tag.

Column classes are prefixed with **clmn**  ranging from 1 to 5 with fractional values represented also.

A classic 2-column layout could be coded as follows:

    <div class="container">
        <div class="row">
            <div class="clmn2"></div>
            <div class="clmn2"></div> 
        </div>
    </div>

A 3-column layout could be coded as follows:

    <div class="container">
        <div class="row">
            <div class="clmn5"></div>
            <div class="clmn3-5"></div> 
            <div class="clmn5"></div>        
        </div>
    </div>
    
A nested column layout could be coded as follows:

    <div class="container">
        <div class="row">
            <div class="clmn2">
                <div class="row">
                    <div class="clmn2"></div> 
                    <div class="clmn2"></div> 
                </div> 
            </div>
            <div class="clmn2"></div>        
        </div>
    </div>

Note the use of the `.row` class to define new rows.

Columns can also be offset.

    <div class="container">
        <div class="row">
            <div class="clmn5 offset4-5"></div>        
        </div>
    </div>
    
Checkout the **index.html** file to see it in action.
