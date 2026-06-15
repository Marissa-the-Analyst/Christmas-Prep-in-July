# Christmas-Prep-in-July
I analyzed a warehouse-style dataset to identify “Christmas Apparel” items and paired them with red/green dog toys and pet hardware for compact, ready-to-deploy side stack displays. Using Excel’s dynamic filters, this approach helps merchandisers quickly build festive, high-impact in-store setups with complementary products. 

# Business Question
Can you get me a list of products that are comin in this Christmas Season and what are some base items we can pair with it? Maybe red and green ones? 

# Finished Product
<img width="1366" height="568" alt="image" src="https://github.com/user-attachments/assets/c08bf12b-e3d5-4bf1-a31f-dedaaf452cb8" />

# Goals
To return two lists of items that would complement each other in a Christmas side stack display to help the marketing team pair complementary items together. 

# Program
- Excel

# Data Source
I got this dataset from Kaggle! Here is the link [Premium Dog Outlets](https://www.kaggle.com/datasets/scoeyd/premium-dog-outlets). The data is synthetic but from my personal experience in a warehouse environment, I found its vastness and general layout to be very familiar! 

# Process
I created a dynamic range using filters and choosecols to extra the “Christmas Apparel” sub-category. <br>

=FILTER(CHOOSECOLS(Product3,1,2,12),Product3[SubCategory]="Christmas Apparel") <br>

Then I created another table using the same method: <br>

=FILTER(CHOOSECOLS(Product3,1,2,12),((Product3[Category]="Dog Toy")*((Product3[Color]="red")+(Product3[Color]="green"))+((Product3[Category]="Pet Hardware")*((Product3[Color]="red")+(Product3[Color]="green"))))) <br>

This formula focused on Dog Toys and Pet Hardware as complementary items on display together. To ensure both options were reserved to red and green, I nested the red and green colors into each category statement.  

# Example Use Case
Using this list, a marketing associate could generate a sample side stack display similar to the following: <br>
<img width="531" height="640" alt="image" src="https://github.com/user-attachments/assets/65554ff6-106f-4682-be54-c97d03d7eada" /> <br>

The numbers representing the unique item numbers allow merchandising partners to have an easy quick reference for how to set up and build these displays before shipping them in through the distribution centers.  
