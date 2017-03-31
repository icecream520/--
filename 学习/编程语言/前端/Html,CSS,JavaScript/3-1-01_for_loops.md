#FOR LOOPS#
<!doctype html>
<html>
    <head>
        <script>
            var continents = ["Australia", "Africa", 
                              "Antarctica", "Eurasia", "America"];
            var response, count = 0;
          
            for (var index=0; index < continents.length; 
                              index++) {
                response = confirm("Have you been to " + 
                                    continents[index] + "?");  
                if (response) count++;
            }
            alert("You have been to " + count + 
                  " continents!");
        </script>
    </head>
</html>
## FOR ... IN LOOPS ##
for ... in gives you the index of each item
<!doctype html>
<html>
    <head>
        <script>
            var continents = ["Australia", "Africa", 
                              "Antarctica", "Eurasia", "America"];
            var response, count=0;
            
            for (var index in continents) {
                response = confirm("Have you been to "
                                   + continents[index] + "?");  
                if (response) count++;
            }
            alert("You have been to " + count +
                  " continents!");
        </script>
    </head>
</html>
## FOR ... IN LOOPS ##
This example shows how for ... in can be used
to access the content of a data structure
 <!doctype html>
<html>
    <head>
        <title>Example of for in</title>
        <script>
            var response, count = 0;
            var onePerson = { initials:"DR", age:40,
                              job:"Professor" };
            
            for (var property in onePerson) {
                alert(property + "=" + onePerson[property]);
            }
        </script>
    </head>
</html>

## FOR ... OF LOOPS ##
<!doctype html>
<html>
    <head>
        <title>Example of for of</title>
        <script>
            var continents = ["Australia", "Africa",
                              "Antarctica", "Eurasia", "America"];
            var response, count = 0;
            
            for (var continent of continents) {
                response = confirm("Have you been to " + 
                                    continent + "?");  
            if (response) count++;
            }
            alert("You have been to " + count + " continents!");
        </script>
    </head>
</html>
var number=1;
for ( ; number <= 12; number++ ) {
alert(number + " times 9 = ", number * 9);
}
var number=1;
for ( ; number <= 12; number++ ) {
alert(number + " times 9 = ", number * 9);
}