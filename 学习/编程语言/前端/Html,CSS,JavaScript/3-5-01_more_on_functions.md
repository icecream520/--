# MORE ON FUNCTIONS #
<!doctype html>
<html>
    <head>
        <script>
            function check(a, b){
                if (b != 0) return true;
                else return false;
            }
            function myDivide( fn, num, div ) {
                if (fn(num, div)) {
                    alert("It's OK!");
                    return num / div;
                } else {
                    alert("Not OK!");
                }
            }

            result=myDivide(check, 44, 1);
            //参数是一个函数加数字
        </script>
    </head>
</html>

<!doctype html>
<html>
    <head>
        <script>
            function counter() {
                var count = 0;

                return function() {
                    count++;
                    alert(count);
                }

            }
            var count = counter();
            //这一步返回的是一个函数，不会执行内部
            count();
            count();
            count();
        </script>
    </head>
</html>
