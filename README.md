# Kaggle-Cassava-Leaf-Disease-Classification
Code for the competition "Cassava Leaf Disease Classification" in Kaggle. Rank 256/3900(Top 7%) Broze Medal

The competition ended in February, and when I was sorting out the code recently, I decided to release it on GitHub (Sorting out the code is really a tired work~).

I got **0.8987** in private dataset. However, it was not my best solution (Determination is the key to success...lol).

The code I released on Github got **0.9010**, which should rank in **silver medal region** if I submitted this solution.

This repo contains the code of training part and testing part, I use some tricks as follows:
- AMP for faster training (GPU time limitation in Kaggle, and I don't have a good GPU)
- Data Aug for better performance(I give up some tricks like cutmix or snapmix, which waste lots of time and didn't improve the performance)
- K fold model ensemble: $k=5$
- Model ensemble: EfficientB4(trained by myself) + Resnext(open access in discussion region)
- Test Time Augmentation: I used a heavy TTA for EfficientB4.

As a kaggle beginner, I learned a lot from this competition, such as some useful tricks for better performance, we should put all config parameters in a file(usually called `config.py`) and so on...

Hope I can get better rankings next time and become a `Kaggle Expert`.
