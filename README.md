# The NLPypline framework

NLPypline is a Python framework for rapidly developing NLP pipelines. It provides much of the common infrastructure shared among many different kinds of pipelines: reading in data, passing data with modifications from stage to stage, featurizing data for each model, training and testing models, decoding the outputs of structured prediction models, evaluating outputs, writing outputs back out, cross-validation of the entire pipeline, and more.

The package is designed for experimentation, so that pipelines can be coded up quickly and stages/models can be swapped in and out easily (to the extent that later stages have not been implemented to rely on the particulars of earlier stages). In a sense, then, it is like a much lighter-weight version of [UIMA](https://uima.apache.org/) for Python, tailored more for rapid exploration than careful system design.

The framework depends on several Python packages, including:
 * Gflags
 * NLTK
 * NumPy/SciPy
 * Scikit-learn
 * [python-crfsuite](https://github.com/scrapinghub/python-crfsuite)
 * Cython (for `src/nlpypline/util/streams.pyx`)
 * mock

NLPypline was developed for and has so far only been used in the [Causeway](https://github.com/duncanka/causeway) project. Aspects of the framework may be too closely tailored to this project, and it is missing important pieces of functionality, but I would love to make it more broadly useful. Please [contact me](mailto:jdunietz@cs.cmu.edu) if you are interested in using NLPypline, and I will happily help you get up and running with it. (Proper documentation will be written up if enough people express interest.)
