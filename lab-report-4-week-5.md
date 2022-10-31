# Lab Report - *Week 5*
## Researching Commands
#### *October 31, 2022*
&nbsp;

## Alternate Command-Line Options for `grep`
&nbsp;

### ***-v: invert match***
&nbsp;

#### **Example 1**
```diff
grep -v a plos/journal.pbio.0020047.txt

needs.
        
to us in the first person, but one is not quite sure which person (the neuroscientist, the
clever word choice.
In short, 
```
This command searches every line of the given file, in this case journal.pbio.0020047.txt, for the lowercase letter "a." However, instead of printing every line that contains "a" it actually does the opposite, and prints every line that does *not* contain "a."

&nbsp;
#### **Example 2**
```diff
grep -v 1 biomed-sizes.txt

527    3455   27953 technical/biomed/ar409.txt
     467    3365   25700 technical/biomed/ar624.txt
     506    3577   27848 technical/biomed/ar745.txt
     639    4538   35253 technical/biomed/ar79.txt
     460    3340   25237 technical/biomed/ar792.txt
     695    5454   40398 technical/biomed/bcr284.txt
     459    3207   25685 technical/biomed/bcr294.txt
     840    5653   44544 technical/biomed/bcr45.txt
     378    2683   20468 technical/biomed/bcr570.txt
     406    2996   22429 technical/biomed/bcr588.txt
     788    6242   46272 technical/biomed/bcr605.txt
     370    2785   20662 technical/biomed/bcr607.txt
     428    2704   22668 technical/biomed/cc3.txt
     439    3082   23472 technical/biomed/cc300.txt
     855    5542   43694 technical/biomed/cc4.txt
     684    5099   39368 technical/biomed/gb-2002-3-5-research0020.txt
     524    3922   30444 technical/biomed/gb-2002-3-7-research0032.txt
     955    4297   36803 technical/biomed/gb-2002-3-7-research0037.txt
     970    5708   45928 technical/biomed/gb-2002-3-9-research0048.txt
     572    3742   29598 technical/biomed/gb-2002-3-9-research0049.txt
     726    5023   39796 technical/biomed/gb-2003-4-5-r32.txt
     684    5064   37359 technical/biomed/gb-2003-4-7-r46.txt
     532    3780   29369 technical/biomed/gb-2003-4-8-r50.txt
     666    4920   35998 technical/biomed/gb-2003-4-9-r57.txt
     569    3573   27080 technical/biomed/gb-2003-4-9-r58.txt
     476    3404   27689 technical/biomed/gb-2003-4-9-r60.txt
     574    3948   32562 technical/biomed/rr37.txt
     426    2847   22290 technical/biomed/rr74.txt
```
This command searches the file biomed-sizes.txt for any line that contains the number 1, and prints every line that does not contain the number.

&nbsp;
#### **Example 3**
```diff
grep -v the pmed.0020281.txt

whistleblowing—as discussed, in part, in 
        courageous men and women [1, 2] For that reason, those of us who congregated in Washington,
        research.
        misrepresented pharmaceuticals; clinical research trial results that have been sequestered
        pharmaceuticals that are detailed to physicians, not to save lives or necessarily improve
        corporations and political interests whose operations we occasionally challenge. Our goal
        assault of unprecedented odds against being heard put forth by that sum of political power,
        expediency, and money.
        A whistleblower's success depends upon competent and articulate media. The debate to
        making—cannot proceed or flourish without it.
        Ralph Waldo Emerson, American essayist and philosopher (1803–1882), commented about
        this is to have succeeded [as a whistleblower].”
```
This command searches the file pmed.0020281.txt for any line that contains "the" or words containing "the." It then prints every line that does not contain "the."


&nbsp;
### ***-c: output count of matching lines only***
&nbsp;

#### **Example 1**
```diff
grep -c results 1468-6708-3-7.txt
5
```
This command searches the given file, 1468-6708-3-7.txt, for the string "results." It then prints the amount of lines that contain "results" which in this case is 5.
&nbsp;
#### **Example 2**
```diff
grep -v -c 'click here for file' 1471-2105-3-30.txt
885
```
This command searches the file 1471-2105-3-30.txt for any instances of the phrase 'click here for file.' However, because -v is also in the command, it actually prints the amount of lines that do NOT contain this line. 
&nbsp;
#### **Example 3**
```diff
grep -w -c the 1471-2148-3-7.txt
277
```
This command, although similar to the first one, is different. The -w specifies that it should search the file 1471-2148-3-7.txt specifically for the word "the", which does not include words that contain "the." It then prints the amount of lines in the file that contain "the."
&nbsp;
### ***-l: output matching files only***
&nbsp;

#### **Example 1**
```diff
grep -l "1471" biomed/*
biomed/1471-2202-2-8.txt
biomed/1471-2202-2-9.txt
biomed/1471-2474-2-3.txt
```
This command lists the directories of the files in ./technical/biomed that contain the number 1471 in them.
#### **Example 2**
```diff
grep -l "chapter" 911report/*
911report/chapter-1.txt
911report/chapter-10.txt
911report/chapter-11.txt
911report/chapter-12.txt
911report/chapter-13.1.txt
911report/chapter-13.3.txt
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-2.txt
911report/chapter-3.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-8.txt
911report/chapter-9.txt
```
This command lists the directories of the files in ./technical/911report that contain the word chapter in them.
#### **Example 3**
```diff
grep -l "jurisdiction" government/About_LSC/*
government/About_LSC/LegalServCorp_v_VelazquezDissent.txt
government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt
government/About_LSC/commission_report.txt
```
This command lists the directories of the files in ./technical/government/About_LSC that contain the word jurisdiction in them.