# IrishTwitterPOS
Irish Twitter POS tagging


The following files are part of the Fulbright Irish Twitter research project (Fulbright Enterprise-Ireland Award 2014-2015):

The project involves the development of a gold-standard POS-tagged corpus of 1537 Irish Tweets. A number of statistical POS tagging models were also trained during this project. All details are published in:
Lynn, Teresa, Kevin Scannell and Eimear Maguire, Minority Language Twitter: Part-of-Speech Tagging and Analysis of Irish Tweets. In Proceedings of the 1st Workshop on Noisy User-generated Text (W-NUT 2015).

========================
# Files
========================


The files we provide here are the training, development and test sets of our best performing models.

STATISTICS:

* Training (1242 tweets)
* Test (148 tweets)
* Development (147 tweets)


ARK:

The ARK format follows:
Format = TOKEN \t TAG   or LEMMA \t TAG

We provide here two versions of the files in the ARK format:
/ark/base 
/ark/lemma


We also provide the bootstrapped version of this best training set - which includes 3198 general domain POS-tagged sentences from Ui Dhonnchadha.[1]

========================
# Models
========================

We do not provide the models in this repository, but they can be induced using this training data on the Twitter POS-tagger developed at CMU [2][3]. We refer to it in our experiments as the ARK POS-tagger.

http://www.ark.cs.cmu.edu/TweetNLP/#pos

Training Command (replace variable names with directory and file names):
java -Xmx12g -cp ark-tweet-nlp-0.3.2.jar cmu.arktweetnlp.Train $workDir/$trainFile $modelDir/$modelFile

Predict/ Test Command:
java -Xmx20g -cp ark-tweet-nlp-0.3.2.jar cmu.arktweetnlp.RunTagger --input-format conll --model $modelDir/$model $workDir/$testFile > $workDir/$predFile


Please email tlynn at computing dot dcu dot ie if the other training/ test/ dev files are required.


========================
# References
========================


[1] Ui Dhonnchadha, E. (2009). Part-of-Speech Tagging and Partial Parsing for Irish using Finite-State Transducers and Constraint Grammar.
     PhD thesis, Dublin City University.

[2] Kevin Gimpel, Nathan Schneider, Brendan O’Connor, Dipanjan Das, Daniel Mills, Jacob Eisenstein, Michael Heilman, Dani Yogatama, Jeffrey Flanigan, and Noah A. Smith. 2011. Part-of-speech tagging for Twitter: Annotation, features, and experiments. In Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human Language Technologies: Short Papers - Volume 2, HLT ’11, pages 42–47, Stroudsburg, PA, USA. As- sociation for Computational Linguistics.


[3] Olutobi Owoputi, Brendan O’Connor, Chris Dyer, Kevin Gimpel, Nathan Schneider, and Noah A. Smith. 2013. Improved part-of-speech tagging for online conversational text with word clusters. In Proceedings of the 2013 Conference of the North American Chapter of the Association for Computa- tional Linguistics: Human Language Technologies, pages 380–390, Atlanta, Georgia, June. Association for Computational Linguistics.


