# Retos PicoCTF


## Objetivo 

Unzip this archive and find the file named 'uber-secret.txt'

## Solución 

```
jesus@jesus-ThinkPad-T420:~$ cd Descargas/
jesus@jesus-ThinkPad-T420:~/Descargas$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
jesus@jesus-ThinkPad-T420:~/Descargas$ cd files/
jesus@jesus-ThinkPad-T420:~/Descargas/files$ find uber-secret.txt
find: ‘uber-secret.txt’: No existe el archivo o el directorio
jesus@jesus-ThinkPad-T420:~/Descargas/files$ find . uber-secret.txt
.
./13771.txt.utf-8
./adequate_books
./adequate_books/more_books
./adequate_books/more_books/1023.txt.utf-8
./adequate_books/more_books/.secret
./adequate_books/more_books/.secret/deeper_secrets
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
./adequate_books/46804-0.txt
./adequate_books/44578.txt.utf-8
./satisfactory_books
./satisfactory_books/more_books
./satisfactory_books/more_books/37121.txt.utf-8
./satisfactory_books/16021.txt.utf-8
./satisfactory_books/23765.txt.utf-8
./acceptable_books
./acceptable_books/17879.txt.utf-8
./acceptable_books/more_books
./acceptable_books/more_books/40723.txt.utf-8
./acceptable_books/17880.txt.utf-8
./14789.txt.utf-8
find: ‘uber-secret.txt’: No existe el archivo o el directorio
jesus@jesus-ThinkPad-T420:~/Descargas/files$ cat ./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
jesus@jesus-ThinkPad-T420:~/Descargas/files$ 

```

## Notas adicionales 
find encuentra archivos, especificando desde donde debe empezar a buscar y el nombre del archivo 
## Referencias 
