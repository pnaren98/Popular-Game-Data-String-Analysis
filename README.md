# Popular-Game-Data-String-Analysis-Project
Uses intermediate level Python programming techniques, including object-oriented programming, list comprehension, string manipulation, and datetime manipulation to find the individual words associated with the most popular games in any given stretch of time.

# Let's Get Started
This project creates a simple set of objects and methods that iterate over a dataset of popular video games. The goal is to find the individual words in the summaries and reviews columns that are associated with the highest rated games. Most of these words will be obviously positive, such as "great" or "outstanding," but some words might give valuable insights about consumer tastes in gaming.
# 1-2
This program only needs two modules- pandas and datetime. We start by importing these modules and then reading the game dataset. After that, we modify the dataframe to make it ready for processing, which involves the obvious removing of NA values and duplicates, but also making sure that every value in the 'Release Date' column is a standardized datetime type.
# 3-6
Cells #3-6 crudely display my method of harvesting the "most positive" words and the ratings associated with them. The methods I use include split() to obtain each "word" separated by spaces, isalpha() to remove the strings with numbers and non-alphabetic symbols, list(set()) to remove all duplicate strings, list comprehension, and finally:
- matching the highest average ratings to their corresponding words by filling a list with each word's "average rating".
- sorting them from highest to lowest in another list.
- indexing the top 10 ratings to their positions in the non-sorted list. 
- matching the yielded indices to the corresponding indices in the list of words. 
The result is a list of the words associated with the highest rated games and another list of those games' average ratings. I do this for words in both the "Reviews" and "Summary" columns.
# 7-10
The above demonstrations were somewhat messy, so I repeat them in a more streamlined set of classes and objects. The first class can retrieve the top 10 words from either the "Reviews" or "Summary" columns. It also puts the words in a dictionary form to make the results more understandable. Finally, it can find the top 10 words for games released only within a stretch of years. The second class is a subclass, which finds the games with reviews or summaries that contain each word in the dictionary, based on the "ranking" of each word by average rating.
As you can see, in the period from 2015 to 2022, the review word "themes" was associated with the highest rated games on average. Does that mean that consumers tended to rate games with deep artistic or philosophical themes highly? Games that had the word "themes" in their reviews include the likes of Disco Elysium, The Last of Us Part II, Soma, and the latest Danganronpa game, so perhaps this supposition is correct. Meanwhile, based on game summaries the word "solve" is associated with the highest rated games. Based on the word's association with games like The Witcher 3, Deltarune, and AI: The Somnium Files, perhaps this means that consumers enjoy games with mystery and intrigue?

Link to Data: https://www.kaggle.com/datasets/arnabchaki/popular-video-games-1980-2023
