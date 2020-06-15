
## Tables
- Basic Table Structure

`<table>` 

`<tr>`

`<td>15</td>`

`<td>15</td>`

`<td>30</td>`

`</tr>`

`<tr>`

`<td>45</td>`

`<td>60</td>`

`<td>45</td>`

`</tr>`

`<tr>`

`<td>60</td>`

`<td>90</td>`

`<td>90</td>`

`</tr>`

`</table>`


<table>
<tr>
<td>15</td>
<td>15</td>
<td>30</td>
</tr>
<tr>
<td>45</td>
<td>60</td>
<td>45</td>
</tr>
<tr>
<td>60</td>
<td>90</td>
<td>90</td>
</tr>
</table>

## WAYS TOCREATE OBJECTS 
### CREATE THE OBJECT, THEN ADD PROPERTIES & METHODS
- LITERAL NOTATION

var hotel = {}

hotel .name= 'Quay';

hotel .rooms = 40;

hotel.booked = 25;

hotel.checkAvailabil ity =function()

return this . rooms - this .booked;

} ;
- OBJECT CONSTRUCTOR NOTATION

var hotel = new Object();

hotel.name = 'Quay';

hotel .rooms = 40 ;

hotel . booked= 25;

hotel.checkAvailability =function()

return this .rooms - this .booked;

} ;

### CREATING AN OBJECT WITH PROPERTIES & METHODS
- LITERAL NOTATION
var hotel = {

name: 'Quay' ,

rooms: 40,

booked: 25,

chec kAvailability: function() {

return this.rooms - this .booked;

}

} ;
