
###### BASIC LEVEL PART 1: Read in the data with csv.reader() and store it in a list of lists called 'data'
import csv
with open('chipotle.tsv', 'rU') as f: 
    data = [row for row in csv.reader(f, delimiter ='\t')] 


###### BASIC LEVEL PART 2: Separate the header and data into two different lists.
header = data[0]
data = data [1:]


###### INTERMEDIATE LEVEL PART 3: Calculate the average price of an order. 

order_no=[row[0] for row in data]
order_no=set(order_no)


price = [float(row[4].strip('$')) for row in data]

average =round(sum(price)/len(order_no),2)

###### INTERMEDIATE LEVEL PART 4: Create a list (or set) of all unique sodas and soft drinks that they sell. 
###### Note: Just look for 'Canned Soda' and 'Canned Soft Drink', and ignore other drinks like 'Izze’.

drinks_list=[]
desc = [row[2]+row[3] for row in data]
for i in range (0,len(desc)):
    if "Canned" in desc[i]:
        drinks_list.append(desc[i])
    elif "Drink"in desc[i]:
        drinks_list.append(desc[i])
    elif "Soda" in desc[i]:
        drinks_list.append(desc[i])    
    
drink_set=set(drinks_list)


###### ADVANCED LEVEL PART 5: Calculate the average number of toppings per burrito. 
###### Note: Let's ignore the 'quantity' column to simplify this task. 
###### Hint: Think carefully about the easiest way to count the number of toppings!

###### ADVANCED LEVEL PART 6: Create a dictionary in which the keys represent chip orders and the values represent the total number of orders. Expected output: {'Chips and Roasted Chili-Corn Salsa': 18, ... } Note: Please take the 'quantity' column into account! Optional: Learn how to use 'defaultdict' to simplify your code.

###### BONUS: Think of a question about this data that interests you, and then answer it!


