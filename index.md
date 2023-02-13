# CSE15L Lab Reports 3
In this lab report, I will demonstrate `less` command with its command-line options.<br> <br> 

The path of the directory I used is `written_2/travel_guides/berlitz1`.<br><br> 

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

**Opition 2** `less -p`<br>
`less -p` will highlight the words which match the given pattern follow by the p. <br>

Put `less -poffer  written_2/travel_guides/berlitz1/HandRIbiza.txt` in the terminal, the output will be:

![a14316fb44fa69704190416c06c4cc8](https://user-images.githubusercontent.com/102566928/218374676-ea167caa-c8cb-4395-8131-1b9d021004e6.png)

Using a different word `less -pHotels written_2/travel_guides/berlitz1/HandRIstanbul.txt`, the output will be:
![f05aab37bfbccd9a18e88e36a01276e](https://user-images.githubusercontent.com/102566928/218375130-9ca50306-d3b6-4d76-ab9c-aa3bb4f8b8fc.png)<br>

From the above output, 'less -p' will display the relative content which contains the first word which matches the pattern after the `p`. You should notice that the pattern match is case-sensitive.<br> 

For example, I type `less -photels written_2/travel_guides/berlitz1/HandRIstanbul.txt`
![9056b5aaa3f9ef167f74b763f349d19](https://user-images.githubusercontent.com/102566928/218377627-b081aaf3-94c9-46c7-87b5-4aff83f39df8.png)

The above command will give the highlight of the "hotel" in a different location since its first letter "h" is not capitalized.

**Opition 3** `less -s`<br>
`less -s` will remove duplicate blank lines in the files, allowing more contents to display.<br>

For example, when just use `less  written_2/non-fiction/OUP/Berk/ch2.txt`, the output is like:

```
than is common in American schools. When asked why children look at each others’ work, kibbutz pupils mention the importance of connecting with others to acquire new skills. They explain, “If your picture looks crooked, you would want to see your friend’s paper to learn how to make it straight,” or “If you aren’t sure what you’re supposed to do, then you should check.” To the same question, American and Israeli urban children typically respond, “I would want to see whose picture was the best,” or “I might be wondering whether she got more right than I did.”5


from interdependency to autonomy

Vygotsky, who studied and wrote about children’s development in Russia in the early twentieth century, was deeply interested in how interdependency—children’s close ties to their community—can pave the way to competence and autonomy. His sociocultural theory has thoroughly collectivist cultural roots. Vygotsky stressed that children need social interaction and meaningful activities to develop, and he regarded high intrinsic motivation and mature, independent functioning as arising from the support granted by cultural experts as children attempt ever more challenging tasks. The child’s mind, Vygotsky pointed out, “extends beyond the skin” and is inseparably joined with other minds. Out of this interconnection springs mastery, proﬁciency, and self-conﬁdence.6
```

When add `-s` option after `less`: `less -s  written_2/non-fiction/OUP/Berk/ch2.txt`, the output will be:

```
than is common in American schools. When asked why children look at each others’ work, kibbutz pupils mention the importance of connecting with others to acquire new skills. They explain, “If your picture looks crooked, you would want to see your friend’s paper to learn how to make it straight,” or “If you aren’t sure what you’re supposed to do, then you should check.” To the same question, American and Israeli urban children typically respond, “I would want to see whose picture was the best,” or “I might be wondering whether she got more right than I did.”5

from interdependency to autonomy

Vygotsky, who studied and wrote about children’s development in Russia in the early twentieth century, was deeply interested in how interdependency—children’s close ties to their community—can pave the way to competence and autonomy. His sociocultural theory has thoroughly collectivist cultural roots. Vygotsky stressed that children need social interaction and meaningful activities to develop, and he regarded high intrinsic motivation and mature, independent functioning as arising from the support granted by cultural experts as children attempt ever more challenging tasks. The child’s mind, Vygotsky pointed out, “extends beyond the skin” and is inseparably joined with other minds. Out of this interconnection springs mastery, proﬁciency, and self-conﬁdence.6
```
Another example:<br>

Before using `-s` option, `less  written_2/non-fiction/OUP/Rybczynski/ch1.txt`:

```
the look of architecture






one
dressing up


Architecture is hard to define. Goethe called it music frozen in space, which, while it captures a sense of rhythm, is too one-dimensional. And it relegates the mot
```

After using `-s` option, `less -s  written_2/non-fiction/OUP/Rybczynski/ch1.txt`:
```
the look of architecture

one
dressing up

Architecture is hard to define. Goethe called it music frozen in space, which, while it captures a sense of rhythm, is too one-dimensional. And it relegates the mother of the arts to an inferior position; just as well to describe music as melted architecture. Nietzsche believed that architecture reflected his pride, man’s triumph over gravity, and his will to power. This notion applies to many buildings, from Gothic cathedrals to skyscrapers, but it is too, well, Nietzschean. The British master Edwin Lutyens referred to architecture as a sort of play: “In architecture, Palladio is the game!” Le Corbusier described his art as “the masterly, correct and magnificent play of masses brought together in light,” which is a good description of one of his own buildings. I am partial to Sir Henry Wotton’s definition. Wotton, who lived a long time in Venice and was a lover of architecture though not an architect, published a treatise on the subject in 1642. “In Architecture, as in all other Operative Arts, the end must direct the Operation,” he wrote. “The end is to build well. Well-building hath three conditions: Commoditie, Firmeness, and Delight.”
```
Thus, we can see using `-s` option help the user to save much more spaces by removing the duplicate blank lines, which is useful when user want the screen to display more contents.

**Opition 4** `less -M`<br>
`less -M` will display the reading statistics when the user is reading the file such as current line number and percentage of content being read
When enter `less -M written_2/travel_guides/berlitz1/HandRIbiza.txt`, the information will be displayed on the bottom.
```
        Recommended Hotels
        The establishments listed below offer a cross-section of
        local restaurants, and should convince you that not everything on the
        island comes with chips (french fries).
        The star rating in brackets after each entry refers to the
        offfical government rating system.
        As a basic guide, the symbols we use indicate what you can
        expect to pay for a three-course meal for two, excluding wine, tax and
        tip. Drinks will add considerably to the final bill.
        ✪less than 5,000 ptas.
written_2/travel_guides/berlitz1/HandRIbiza.txt lines 2-15/20 87%
```
Here, `written_2/travel_guides/berlitz1/HandRIbiza.txt lines 2-15/20 87%` is the information provided by the `-M` option.<br>

Another example is `less -M written_2/non-fiction/OUP/Berk/ch2.txt`:
```
Talia and Jim’s fear of helping 7-year-old Anselmo with his homework, lest they create a dependent, immature child, is a peculiarly Western—and profoundly American—preoccupation. American middle-class parents typically regard young children as dependent beings who must be urged toward independence. In response to researchers’ queries, they frequently say that babies should be trained to be self-reliant from the ﬁrst few months.1 Consequently, they place a high value on children’s learning and doing on their own. Repeatedly relying on others for assistance is construed as weakness, uncertainty, and lack of capacity. In keeping with this view, many American parents worry that if their children seek help, they may become dependent.
A similar view permeates traditional classrooms, where an individualistic value system prevails. Children must “do their own work.” In the most intensely individualistic of these settings, conferring with your neighbor is worse than dependency; it is cheating, and teachers go so far as to set up barriers between pupils, such as upright books and cardboard screens, to prevent it.
This emphasis on independent accomplishment is not broadly accepted around the world. Indeed, adults in some non-Western cultures regard American parents as rather merciless in pushing their young children toward independence—for example, when they insist that infants sleep alone rather than with their parents, or when they take pleasure in the earliest possible mastery of motor skills, such as crawling and walking, long before the child has acquired the reasoning powers to avoid steep stai
written_2/non-fiction/OUP/Berk/ch2.txt lines 2-7/248 2%
```
Here, `written_2/non-fiction/OUP/Berk/ch2.txt lines 2-7/248 2%` is the information provided by the `-M` option.<br>

`-M` option is useful when the user need to know the current progress of reading, and user is able to know the current line number by just looking the information on the bottom.
