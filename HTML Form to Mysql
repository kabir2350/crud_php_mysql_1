
    <!DOCTYPE html>
    <html>
    <head>
    <title>HTML Form to Mysql</title>
    </head>
    <body>
    <form method="post" action="#">
    Username : <input type="text" name="username"><br><br>
    Password : <input type="password" name="password"><br><br>
    Info: <input type="text" name="info"><br><br>
    <input type="submit" value="Submit" id="postform">
    </form>

    
    <?php

            $host = "localhost";
            $dbusername = "root";
            $dbpassword = "";
            $dbname = "test";
            $conn = new mysqli ($host, $dbusername, $dbpassword, $dbname);
            if (mysqli_connect_error()){
            die('Connect Error ('. mysqli_connect_errno() .') '
            . mysqli_connect_error());
            }
                  
        
    $username = filter_input(INPUT_POST, 'username');
    $password = filter_input(INPUT_POST, 'password');
    $info = filter_input(INPUT_POST, 'info');


    if (!empty($username)){
        if (!empty($password)){
            $sql = "INSERT INTO demo_profile(username, password,info)
            values ('$username','$password', '$info')";
            if ($conn->query($sql)){
            echo "sucessful entry: ". $username . "_".
            $password . "_".$info ;
            }else{
            echo "Error: ". $sql ."
            ". $conn->error;
            $conn->close();
            }//else ends
        }else{
            echo "Password should not be empty";
            die();
        } //else  ends
    }else{
        echo "username should not be empty";
        die();
    }
   
    ?>

    </body>
    </html>
