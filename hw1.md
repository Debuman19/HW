**Using  chipotle.tsv  in the  data  subdirectory:**

Used **git clone** to clone dat9 onto computer and access data subfoler

####1. Look at the head and the tail, and think for a minute about how the data is structured.

_head chipotle.tsv_

Data is structured as purchase order for food items.

**- What do you think each column means?**

Each column represents a description (label) of the attribute to be recorded. e.g. item name, unit price etc.

**- What do you think each row means?**
 
Each row contains the value of the attribute for a specific order e.g. Quantity ordered, unit price of item

**- How many orders do there appear to be?**

_tail chipotle.tsv_

The last order number in the file is listed as __1834__.

#####- How many lines are in the file?
_wc -l chipotle.tsv_

This command returns a value of __4623__ lines


#####- Which burrito is more popular, steak or chicken?
_grep -i chicken chipotle.tsv > chicken.tsv_                                                                
_wc -l chicken.tsv_                                                           
__1565__ chicken.tsv

_grep -i steak chipotle.tsv > beef.tsv_                                         
_wc -l beef.tsv_                                                                
__706__ beef.tsv

Hence __Chicken__ is more popular

#####- Do chicken burritos more often have black beans or pinto beans?
_grep -i black chicken.tsv > black.tsv_
_wc -l black.tsv_
__759__ black.tsv

_grep -i pinto chicken.tsv > pinto.tsv_
_wc -l pinto.ts_
__265__ pinto.tsv

Hence chicken burritos most often have __black beans__

####2. Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT9 repo.
grep -r dictionary *    
project/README.md:*          
**Data dictionary (aka "code book"):** description of each variable, including units       
README.md:2. Count the number of occurrences of the word 'dictionary' (regardless of case) across all files in the DAT9 repo.




