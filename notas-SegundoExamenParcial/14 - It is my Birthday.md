# Retos PicoCTF


## Objetivo 
I sent out 2 invitations to all of my friends for my birthday! I'll know if they get stolen because the two invites look similar, and they even have the same md5 hash, but they are slightly different! You wouldn't believe how long it took me to find a collision. Anyway, see if you're invited by submitting 2 PDFs to my website. [http://mercury.picoctf.net:50970/](http://mercury.picoctf.net:50970/)

## Solución 

```
<?php  
  
if (isset($_POST["submit"])) {    $type1 = $_FILES["file1"]["type"];    $type2 = $_FILES["file2"]["type"];    $size1 = $_FILES["file1"]["size"];    $size2 = $_FILES["file2"]["size"];    $SIZE_LIMIT = 18 * 1024;  
  
    if (($size1 < $SIZE_LIMIT) && ($size2 < $SIZE_LIMIT)) {  
        if (($type1 == "application/pdf") && ($type2 == "application/pdf")) {            $contents1 = file_get_contents($_FILES["file1"]["tmp_name"]);            $contents2 = file_get_contents($_FILES["file2"]["tmp_name"]);  
  
            if ($contents1 != $contents2) {  
                if (md5_file($_FILES["file1"]["tmp_name"]) == md5_file($_FILES["file2"]["tmp_name"])) {                    highlight_file("index.php");  
                    die();  
                } else {  
                    echo "MD5 hashes do not match!";  
                    die();  
                }  
            } else {  
                echo "Files are not different!";  
                die();  
            }  
        } else {  
            echo "Not a PDF!";  
            die();  
        }  
    } else {  
        echo "File too large!";  
        die();  
    }  
}  
  
// FLAG: picoCTF{c0ngr4ts_u_r_1nv1t3d_73b0c8ad}
```

## Notas adicionales 

## Referencias 
