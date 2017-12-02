# Review Summarization - Aspect based opinion mining
Summarize opinions of users about a product from a set of reviews. Extract the most common product features mentioned, most common opinion words used for a feature and the corresponding positive and negitive opinions about related to the feature and opinions. This way it becomes extremely easy to identify the most prominent positive and negitive features and opinions about a product.

## Methodology:

1. Tokenize the reviews into sentences.

2. Create a set of nouns in each sentence. Extract the most common nouns in all of the reviews using apriori algorithm. This gives us the most frequent features/aspects of the product.

3. Classify each sentence containing a product feature as positive, negitive or neutral using the Liu and Hu opinion lexicon.

4. Extract opinion phrases from sentences using nltk chunking. We identify the most frequent opinion phrases using frequency distribution.

5. For each product feature and corresponding opinion phrase, we display the positive and negitive reviews.


## Sample:

**Product**: phone

**Features**: camera, battery, price, performance

**Opinion Phrases**: great camera, great battery, low light, heat issues

**Output for a feature**:

*Feature* - camera

*Positive* - great camera

*Reviews* -
1. Superb slick phone, great camera nice depth mode like DSLR cameraphone is a beast n crazy fast...I am very happy with the purchase...
2. portrail photo is the awsome feature, perfect andoid product at hisAwesome product with great camera features.. Lighting fast processor...
3. Nice phone with great camera battery backup
4. Amazing phone in good price,with great camera experience

*Negitive* - low light

*Reviews* -
1. low lighting photos could have been better.
2. Camera quality awesome on rear, but struggling on low lighting conditions a little bit as there sometimes appears noise in image captured in low light.
