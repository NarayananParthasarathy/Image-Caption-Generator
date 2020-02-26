Image Caption Generator using different combinations of CNN (VGG/InceptionV3/Xception) & LSTM/GRU

The project is about creating an ‘Image Caption Generator’ using a combination of CNN layers (VGG16/InceptionV3/Xception using transfer learning) & Recurrent networks (LSTM/GRP) for NLP. This model pipeline uses a merge architecture, with the features extracted using the CNN layer and the NLP layer ( cleansed captions passed through a word embedding & then through a LSTM / GRU) are merged (using Keras – Add ) and passed to dense layers.  

Here, we use a combination of data from multiple datasets – Flickr8K, Flickr30K, MS COCO & Google Conceptual Captions to bring diversity. 

Files to be executed in the order of naming ( 1., 2., 3. & 4.) 

1.DataSet_creator_Drive/Local --> For creating data from multiple sources. 

2.Image_Feature_Extractor --> For extracting the features from the images using VGG16/KInceptionV3/Xception & stores in a .pkl file

3.Base_model --> All  train & caption generation part in this. Pipeline is build in such a way to work in a constrained environment of google colab (free).  Model gets saved after every epoch & if colab gets timed out / crashed, then the next execution will pick up the last saved .h5 file

4.Evaluator --> Program to score the generated captions on BLEU, METEOR, ROUGE & SPICE. Input will be the generated (candidate) captions in a file & the master captions (ground truth) in a separate file. SPICE scoring has dependencies (mentioned inside the notebook). 

