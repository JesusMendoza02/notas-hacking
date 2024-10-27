# Retos PicoCTF


## Objetivo 

Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución 

```
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ atril Financial_Report_for_ABC_Labs.pdf 
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ pdftotext Financial_Report_for_ABC_Labs.pdf 
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ pdftotext Financial_Report_for_ABC_Labs.pdf text
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ ls
Financial_Report_for_ABC_Labs.pdf  Financial_Report_for_ABC_Labs.txt  text
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ mv text flag.txt
jesus@jesus-ThinkPad-T420:~/picoCTF/segundoparcial/forensic/redactiongonewrong$ cat flag.txt 
Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.

Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.

```

## Notas adicionales 

## Referencias 
