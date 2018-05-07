# Vietnamese pretrained word2vec model on news dataset.
This is the trained Word2Vec model for Vietnamese language. The model is trained on data crawled from Vietnamese news websites including vnexpress.net, dantri.com.vn, and tuoitre.vn. Currently the crawled data has more than 60,000 articles, with total of 509806 sentences, or 12 millions words. The model can be directly used to derived the vector representation of words. 

A. Example  
For example, 'vua' (king) is similar to 'Tự_Đức' (Vietnam's last king), and 'lăng_mộ' (tomb). This mean most context from local news mentions 'vua' and 'Tự_Đức', and they are interchangable in many context.

Top 10 most similar words to 'vua', and their similarity scores:  
```
Tự_Đức 0.757419407368  
lăng_mộ 0.754067182541  
Gia_Long 0.704775929451  
thờ 0.668936312199  
Quang_Trung 0.662353932858  
mộ 0.643899619579  
Tây_Sơn 0.638754427433  
Đan_Dương 0.634660363197  
miếu 0.632310509682  
hoàng_đế 0.63085693121  
```

B. How to use  
#Step 1 download the Word2Vec model from think <a href="https://drive.google.com/open?id=10SmNJwPh6d7H7m3SaQoWEwmt06wz8Emd">link</a>  
#Step 2 place the model in the same folder with your working directory and load the model  
```
import gensim  
model = gensim.models.Word2Vec.load('./model_vnnews_w2v')  
```
