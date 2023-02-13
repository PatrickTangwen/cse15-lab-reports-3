# CSE15L Lab Reports 3
In this lab report, I will demonstrate `less` command with its command-line options.<br> <br> 

The path of the file I used is `written_2/travel_guides/berlitz1/IntroFrance.txt`.<br><br> 

The `less` command can show the content of a file in the terminal.Using the basic `less` command without any options, it will temporarily take over your terminal and give a interaction window for the users to scroll up and down. To quit, just type `q` and then it will get back to the normal terminal. When using options,it can help users to navigate the content of a file in different ways.<br><br> 

Below I will demonstrate the differnet opitons with input command and its output.<br>


**Opition 1** `less -N`<br>
`less -N` will show line numbers of each line in the file. <br>

Enter `less -N  written_2/travel_guides/berlitz1/IntroFrance.txt` in the terminal, the output would be:

```   
      1
      2
      3
      4      
      5        
      6         FRANCE AND THE FRENCH
      7         For many years France was a nation of internal contrasts —
      8         between the more urban and industrial north and the rural south,
     ...
    157         delightfully different and comfortably familiar, a country of exciting
    158         and infinitely attractive contrasts.
    159       
    160     
    161   
(END)
```
Using a different file `less -N  written_2/travel_guides/berlitz1/HandRIbiza.txt`, the output would be:
```
      1 
      2   
      3   
      4     
      5       
      6         Recommended Hotels
      7         The establishments listed below offer a cross-section of
      8         local restaurants, and should convince you that not everything on the
      9         island comes with chips (french fries).
     10         The star rating in brackets after each entry refers to the
     11         offfical government rating system.
     12         As a basic guide, the symbols we use indicate what you can
     13         expect to pay for a three-course meal for two, excluding wine, tax and
     14         tip. Drinks will add considerably to the final bill.
     15         ✪less than 5,000 ptas.
     16         ✪✪5,000–8,000 ptas.
     17         ✪✪✪more than 8,000 ptas.
     18       
     19     
     20   
(END)
```
From the above output, it's clear to see that `less -N` will display the content of file line by line with its own line number. It's useful when the user want to look at a specific line by providing the line number for the reader to nagivate the wanted line.

**Opition 2** `less -N`<br>
`less -N` will show line numbers of each line in the file. <br>

```
      
        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that **not** everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
        offfical government rating system.
        As a basic guide, the symbols we use indicate what you can
        expect to pay for a three-course meal for two, excluding wine, tax and
        tip. Drinks will add considerably to the final bill.
        ✪less than 5,000 ptas.
        ✪✪5,000–8,000 ptas.
        ✪✪✪more than 8,000 ptas.
      
    
  
(END)
```
