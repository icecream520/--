#more_on_arrays #
## SORTING ##
array.sort() sorts the elements in array:
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    pets.sort();
// Now pets is ["Cat", "Dog", "Hamster", "Rabbit"]
## REVERSE ##//倒叙排列
array.reverse() reverses array

The first element becomes the last;
The last element becomes the first
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    pets.reverse();
// pets is ["Hamster", "Rabbit", "Cat", "Dog"]
## DESCENDING ORDER ##//降序排序
By combining sort() and reverse(),
you can sort things in descending order:
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    pets.sort().reverse();
// pets is ["Rabbit", "Hamster", "Dog", "Cat"]
## FINDING AN ELEMENT ##
Use array.indexOf(target) to find the index of
the first occurence of target in array:
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    alert(pets.indexOf("Rabbit")); // This shows 2
If target is not in array, indexOf() will return -1
## MORE ON FINDING AN ELEMENT ##

Pass a second value to indexOf()
to control where to start the search
    array.indexOf(target, startPosition)
  
<!doctype html>
<html>
    <body>
        <script>
            var pets = ["Dog", "Cats", "Rabbit", "Hamster",
                        "Rabbit", "Rabbit", "Dog", "Cat",
                        "Hamster", "Hamster", "Rabbit"];//新建数组
            var rabbitPositions = [], startSearchAt = 0;
            
            do {
                foundAt = pets.indexOf("Rabbit", startSearchAt);//从0开始searchAT,得到"Rabbit"的index
                if(foundAt != -1) {//如果找到了
                  rabbitPositions.push(foundAt);//在这个数组里面Push进那个编号
                  startSearchAt = foundAt + 1;//先从0开始如果找了就加一位继续找，直到没有
                }
            } while(foundAt != -1);
            alert(rabbitPositions); // This shows [2, 4, 5, 10]
        </script>
    </body>
</html>
## FINDING ELEMENT BACKWARDS ##
Use array.lastIndexOf(target) to find target in array,
starting from the last element in array:
    var pets = ["Rabbit", "Dog", "Cat",
    "Rabbit", "Hamster"];
    alert(pets.lastIndexOf("Rabbit")); // This shows 3
## SLICE() ##
Extract part of an array by array.slice(startPosition)://从slice标号的数字开始的全部
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    var result = pets.slice(1);
    // result is ["Cat", "Rabbit", "Hamster"]
You can also set where to stop, by
    array.slice(startPosition, endPosition):
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    var result = pets.slice(1, 3);
    // result is ["Cat", "Rabbit"]
## REMOVE SOMETHING ANYWHERE IN AN ARRAY ##
splice() is used when you want to remove
element(s) anywhere from an array
To remove element(s) anywhere from an array, use
array.splice(position, quantity)
    var pets = ["Dog", "Cat", "Rabbit", "Hamster"];
    var result = pets.splice(1, 1);
    // Now pets is ["Dog", "Rabbit", "Hamster"]
    // and result is ["Cat"]
splice() returns the removed element(s)

## ADD SOMETHING ANYWHERE IN AN ARRAY ##
splice()//剪接 can also be used when you want
to add element(s) anywhere to an array

To add an element anywhere to an array, use
array.splice(position, 0, element)
var pets = ["Dog", "Cat", "Hamster"];
var result = pets.splice(2, 0, "Rabbit");
// Now pets is ["Dog", "Cat", "Rabbit", "Hamster"]
// and result is []

Because nothing is removed from pets, result is []

## REPLACE SOMETHING ANYWHERE IN AN ARRAY ##

To replace element(s) anywhere in an array, use
array.splice(position, quantity, element(s))

var pets = ["Dog", "Cat", "Hamster"];
var result = pets.splice(1, 1, "Rabbit", "Fish");//移除1开始的一个元素，同时添加2个元素
// Now pets is ["Dog", "Rabbit", "Fish", "Hamster"]
// and result is ["Cat"]