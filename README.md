# day-4-task
compare two json without order 
var obj1 = {"name":"Sam","class":"MCA"};
var obj2 = {"class":"MCA","name":"Sam"};

var flag=true;

if(Object.keys(obj1).length==Object.keys(obj2).length){
    for(key in obj1) { 
        if(obj1[key] == obj2[key]) {
            continue;
        }
        else {
            flag=false;
            break;
        }
    }
}
else {
    flag=false;
}
console.log("is object equal"+flag);

use the country flags 
fetch('https://restcountries.eu/rest/v2/alpha/cn')
  .then(res => res.json())
  .then(data => initialize(data))
  .catch(err => console.log('Error:', err.message)); // (I fixed this)

// A little destructuring...
function initialize({
  name,
  capital,
  callingCodes,
  population,
  currencies,
  region
}) {
  console.log({
    name,
    capital,
    callingCodes,
    population,
    currencies,
    region
  })
}

