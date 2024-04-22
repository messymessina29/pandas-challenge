# pandas-challenge
I used the AI Xpert Leaning assistant a couple of times to help me with my code of the pandas-challenge.
The first instance was where it asked to count the number of unique schools in the District summary. I was able to get an array of the unique values but I wasn't sure how to count them up. The Ai assistant told me to use the nunique() method instead to get the count of the items in the array. Please see reference below:

    school_count = school_data_complete["school_name"].nunique()

The other instance I used the Ai assistant was to help me with the binning part of the Scores by School Spending. I tried to run the code for the pd.cut but I kept getting an error that had something to do with the "Per Student Budget" column being a string. I used this code shown below to help remove the formatting of the "Per Student Budget" column:

    school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].str.replace("$", "").str.replace(",", "")

I then ran this code on the next line based on prior knowledge on how to convert types:

    school_spending_df = school_spending_df.astype({"Per Student Budget": float}, errors='raise')
    