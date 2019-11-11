# A
Question/need help Statements:

1.) possible redundancy: in var isMobile “ ... iPhone|iPad|iPod ... “ ... is this taken care of via “ ...  i.test(navigator.userAgent) ... “??? (Currently line 28 below)

2.) I suspect error on 1st “ ... IF ... “  line around “ ... && ... “ (Currently line 31 below)

3.) Javascript " ... var isMobile ... " (line 28) below, is meant to have the same result as the PHP " ... return preg_match ... " (on line 61). I am not certain I am calling the Javascript correctly! ??? I would also like to call the PHP, I believe is done correctly, if necessary and then make it talk with the rest of my JS code.

-_______________________-

<!DOCTYPE html>
<html>
<head>
</head>
<body>

<!--
Got tired of button, so I commented it out ...

<button onclick="detectIPadOrientation();">What's my Orientation?</a>

-->

<script type="text/javascript">

   function detectMobileOrientation () {
           var isMobile = /android|avantgo|blackberry|bolt|boost|cricket|docomo|fone|hiptop|iPhone|iPad|iPod|mini|mobi|palm|phone|pie|tablet|up\.browser|up\.link|webos|wos|/i.test(navigator.userAgent);
       var element = document.getElementById('text');
       
       if (Math.abs(window.orientation) === $var && isMobile()) {
           if ($var === 90) {
                   alert ('Landscape Mode, Either Orientation');
                   element.innerHTML = "You are using Mobile";
           }
           else {
                   alert ('Portrait Mode, Either Orientation');
                   element.innerHTML = "You are using Mobile";
           }
       } else {
                 alert ('Desktop');
                 element.innerHTML = "You are using Desktop";
       }

       }

detectMobileOrientation();

window.onorientationchange = detectMobileOrientation;

</script>

       <p id="text"></p>

</body>
</html>

_——————————_

<!-- 

PHP userAgent call ... similar to “ ... var isMobile above ... “ 
<?php

return preg_match("/(android|avantgo|blackberry|bolt|boost|cricket|docomo|fone|hiptop|iPhone|iPad|iPod|mini|mobi|palm|phone|pie|tablet|up\.browser|up\.link|webos|wos)/i", $_SERVER["HTTP_USER_AGENT"]);

?>

-->
